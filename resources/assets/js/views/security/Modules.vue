
<style scoped>

 
</style>

<template>
  <div>
 <mypopup slot="message"></mypopup>
 <myimport slot="modal-import" url-import="security/modules/import"></myimport>
 <mytopmenu show-menu="true"></mytopmenu> 
	<div class="container-fluid">
		<div class="row">
			<div class="col-sm-2">
				<mysubmenu submenu= "security"></mysubmenu>
			</div>
		
			<div class="col-sm-10">

				<mymessage 
					message="moduleTopMessage" 
					color="info"
					align="center"
				>

				</mymessage>
				
				<mycrudtable  

						table-id="table1"

						table-title="moduleList" 

						select-fields='{	}'
									
						columns-names='{
								"0": { "name": "id", "width":"10%"},
								"1": { "name": "moduleName", "width":"25%"},
								"2": { "name": "moduleDescription" , "width":"50%"},
								"3": { "name": "moduleOrder" , "width":"50%"},
								"4": { "name": "status", "width":"10%"},
								"5": { "name": "createdBy", "width":"15%"},
								"6": { "name": "updatedBy", "width":"25%"}
						}' 
						
						url="security/modules"


						icon-info='{	}'
						icon-actions='{		}'

						>
						
				
						<mycrudbuttons 
							slot="crud" 
							url-export="security/modules/export"
							btn-actions='{
         						"0": {"title": "add",    "method": "Add",    "disabled": false},
        						"1": {"title": "export", "method": "Export", "disabled": false}, 
        						"2": {"title": "import", "method": "Import", "disabled": false}        				
        			}'
						>
						</mycrudbuttons>
						
						<mycrudform 
							slot="forma" 

							url="security/modules"

							form-title="module"

							input-fields='{
									"0": {
										"type": "text",
										"name": "id",
										"value": "", 
										"label": "id",	
										"placeholder":"",
										"readonly":"true",
										"required": "true",	
										"maxlength": ""
									},

									"1": {
										"type": "text",
										"name": "module_name",
										"value": "", 
										"label": "moduleName", 
										"placeholder":"Type the Module Name",
										"required": "true",	
										"maxlength": ""
									},

									"2": {
										"type": "textarea",
										"name": "module_description",
										"value": "", 
										"label": "moduleDescription", 
										"placeholder":"Type the Module Description",
										"required": "true",	
										"maxlength": ""
									 },

									"3": {
										"type": "text",
										"name": "module_order",
										"value": "", 
										"label": "moduleOrder", 
										"placeholder":"Type the Module Order",
										"required": "true",	
										"maxlength": ""
									},

									"4": {
										"type": "status",
										"name": "deleted_at",
										"label": "status"
									 }
									
								}'
						>
						</mycrudform>
				</mycrudtable>
			<div>
		</div>
	</div>
 </div>
</template>


<script 

src="../../main.js" type="text/javascript">
	
</script>


<!-- ======= PROPS TO DISPLAY ICON LINKS IN THE TABLE============-->

<!-- icon-info='{
		"0": { "url": "#", "name":"truck", "title":"List Of....", "icon": "fa fa-file-text-o", "text":""},
		"1": { "url": "#", "name":"truck", "title":"List Of....", "icon": "fa fa-truck", "text":""},
		"2": { "url": "#", "name":"truck", "title":"List Of....", "icon": "fa fa-road", "text":""}
}'


icon-actions='{
		"0": { "url": "/users", "name":"truck", "title":"List Of....", "icon": "fa fa-user", "text":""},
		"1": { "url": "#", "name":"truck", "title":"List Of....", "icon": "fa fa-comment-o", "text":""},
		"2": { "url": "#", "name":"truck", "title":"List Of....", "icon": "fa fa-map-marker", "text":""},
		"3": { "url": "#", "name":"user", "title":"List Of....", "icon": "fa fa-trash", "text":""}
}' -->
