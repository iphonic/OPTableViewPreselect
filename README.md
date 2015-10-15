# OPTableViewPreselect
Adding capability of preselecting cell using https://github.com/mbrandonw/OPTableView

This allows you to preselect any cell, that might be useful in some scenarios. All you need to do is to define

    self.tableView.selectionDatasource=self;
 

and return the preselected row number with new `NSIndexPath`

    -(NSIndexPath *)preSelectIndexPath{
       return [NSIndexPath indexPathForRow:10 inSection:0];
    }
    
Works only if `self.tableView.snapToRows=YES;`
