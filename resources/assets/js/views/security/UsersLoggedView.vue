
<style scoped>

	.link-space {
		padding-right: 40px;
	}
 
</style>

<template>

<div>
 	<mypopup slot="message"></mypopup>
	<myimport slot="modal-import" url-import="security/modules/import"></myimport>

	<mytopmenu show-menu="true"></mytopmenu> 
	<div class="container-fluid" >
		
		<div class="row" >
			<div class="col-sm-2">
				<mysubmenu submenu= "security"></mysubmenu>
			</div>
			<div class="col-sm-10" >

				<mymessage 
					message="dashboardTopMessage"
					color="info"
					align="center"
				>
				</mymessage>

				<myhorizontallinks name="horizontal-links"></myhorizontallinks>

	    		<div class="row" style="padding:0px">
					<div class="col-sm-12" style="padding:0px">
					 
					  <div style="padding-left:10px;padding-right:20px">
					  
					  	<mychart 
					  		id="Chart1"
					  		type="spline"
					  		width="500"
					  		height="250"
							  url="/security/dashboard/usersLoggedByDay"
							  title="usersLoggedByDay"
							  x-title="Days"
							  y-title="Users Logged"
							  legend-position="bottom"
							  legend-display="false"
							  show-year="true"
							  show-month="true"
					  	>

					  	</mychart>

					 	</div>
					</div>
				</div>
				
				<div class="row" style="padding:0px">
					<div class="col-sm-6" >
					 
						<mytableyearmonth  

							table-id="table1"

							table-title="topUserLogged" 

							columns-names='{
									"0": { "name": "username", "width":"25%"},
									"1": { "name": "userFullname" , "width":"50%"},
									"2": { "name": "timesLogged" , "width":"50%"}
									
							}' 
							
							url="security/dashboard/usersLogged"

							icon-info='{ }'

							icon-actions='{ }'

							show-year ="true"

							show-month = "true"

							>

							</mytableyearmonth>

						</div>
					

					<div class="col-sm-6" >
					 
					  <mytableyearmonth  

					  			table-id="table2"

									table-title="actionsByUserLogged" 

									columns-names='{
											"0": { "name": "username", "width":"25%"},
											"1": { "name": "actions" , "width":"50%"},
											"2": { "name": "clicks", "width":"10%"}
									}' 
									
									url="security/dashboard/actionsByUsersLogged"

									icon-info='{ }'

									icon-actions='{ }'

									show-year ="true"
							
									show-month = "true"

									>

						</mytableyearmonth>

					</div>
				</div>

				<div class="row" style="padding:0px">
					<div class="col-sm-12" style="padding:0px">
					 
					  <div style="padding-left:10px;padding-right:20px">
					  
					  	<mychart 
					  		id="Chart2"
					  		type="column"
					  		width="500"
					  		height="250"
							  url="/security/dashboard/usersLoggedByMonth"
							  title="usersLoggedByMonth"
							  x-title="Days"
							  y-title="Users Logged"
							  legend-position="top"
							  legend-display="false"
							  show-year="true"
							  show-month="false"
					  	>
					  	</mychart>

					 	</div>
					</div>
				</div>


			</div>		
		</div>		
	</div>
</div>
</template>


<script 

src="../../main.js" type="text/javascript">
	
</script>



										