  
  var change = function(){...}

	function jiexi(obj) {
		for (var key in obj) {
			if (obj.hasOwnProperty(key) === true) {
				if (typeOf(obj[key]) == 'object') {
					jiexi(obj[key]);
				} else {
					obj[key] = change(obj[key]);
				}
			}
		}
	}
 
  给返回的data里面所有的字段 通过change来渲染(加密)
