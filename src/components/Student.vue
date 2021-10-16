<template>

<section>
<h2>Student List</h2>
<div id="content" class="p-4 p-md-5">
    <div class="main-panel">
        <div class="overflow-auto example">
            <table class="table table-striped">
            <thead>
                <tr>
                    <th>User Name</th>
                    <th>Student ID</th>
                    <th>Batch</th>
                    <th>First Name</th>
                    <th>Last Name</th>
                    <th scope="col">Email</th>
                    <th scope="col">Phone</th>
                    <th scope="col">ParentName</th>
                    <th scope="col">Program</th>
                    <th scope="col">Status</th>
                    <th scope="col">Unit</th>
                    <th scope="col">Coach</th>
                    <th scope="col">DOB</th>
                    <th scope="col">Grade</th>
                    <th scope="col">Age</th>
                    <th scope="col">Address</th>
                    <th scope="col">City</th>
                    <th scope="col">Pin</th>
                    <th scope="col">ChessKid</th>
                    <th scope="col">DOR</th>
                    <th scope="col">MOR</th>
                    <th scope="col">DOJ</th>
                    <th scope="col">MOJ</th>
                    <th scope="col">TotalPaidClass</th>
                    <th scope="col">TotalClassTillApril30</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in list" :key="item.id">
                    <td>{{item.username}}</td>
                    <td>{{item.student_id}}</td>
                    <td>{{item.batch}}</td>
                    <td>{{item.first_name}}</td>
                    <td>{{item.last_name}}</td>
                    <td>{{item.email}}</td>
                    <td>{{item.phone}}</td>
                    <td>{{item.parent_name}}</td>
                    <td>{{item.program}}</td>
                    <td>{{item.status}}</td>
                    <td>{{item.unit}}</td>
                    <td>{{ }}</td>
                    <td>{{item.dob}}</td>
                    <td>{{item.grade}}</td>
                    <td>{{item.age}}</td>
                    <td>{{item.address1}}</td>
                    <td>{{item.city}}</td>
                    <td>{{item.pin}}</td>
                    <td>{{item.chesskid}}</td>
                    <td>{{item.DOR}}</td>
                    <td>{{item.MOR}}</td>
                    <td>{{item.DOJ}}</td>
                    <td>{{item.MOJ}}</td>
                    <td>{{item.TotalPaidClass}}</td>
                    <td>{{item.TotalClassTillApril30}}</td>
                </tr>
            </tbody>
            </table>
        </div>
    </div>
</div>
</section>


</template>


<script>

import axios from "axios"

export default {
    name: 'App',
    data()
    {
        return {
        list:[]
        }
    },
    async mounted()
    {
        let result = await axios.get("https://3.7.128.140:9083/student/api/list/SuperUser");
        console.warn(result.data.studentData)
        this.list=result.data.studentData
    },
};

</script>


<style>
  .table-style1 thead th {
   background-color: red;
   color: white;
   vertical-align: middle; 
   text-align: center;
}
</style>