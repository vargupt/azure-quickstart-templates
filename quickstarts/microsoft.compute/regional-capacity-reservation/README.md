
**On-demand-capacity-reservation**

This template can be used to deploy a regional capacity reservation group and a capacity reservation for Standard_D2s_v3 VMs.

On-Demand Capacity Reservation enables customers to reserve Compute capacity in an Azure region or an Availability Zone for any duration of time. Unlike Reserved Instances, customers don't have to sign-up for a 1-year or a 3-year term commitment. They can create and delete reservations at any time and have full control over how they want to manage their reservations. Once the capacity reservation is created, the capacity is available immediately and is exclusively reserved for the customer until the reservation is deleted. Capacity Reservation has some basic properties that are always defined at the time of creation: • VM size - Each reservation is for one VM size. For example, Standard_D2s_v3. • Location - Each reservation is for one location (region). If that location has availability zones, then the reservation can also specify one of the zones. • Quantity - Each reservation has a quantity of instances to be reserved.

To create a Capacity Reservation, these parameters are passed to Azure as a capacity request. If the subscription lacks the required quota or Azure does not have capacity available that meets the specification, the reservation will fail to deploy. Either request more quota or try a different VM size/location/zone combination.

Once Azure accepts a reservation request, it is available to be consumed by VMs of matching configurations. In order to consume capacity reservation, VM will have to specify the reservation as one of its properties. Otherwise, the capacity reservation will remain unused. One benefit of this design is that customers can target only the mission critical workloads to reservations and other non-critical workloads can run without reserved capacity.

**Reference** 
References to On-demand Capacity Reservation documentation will be added once publicly available
