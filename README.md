# ♻️ Landfill Network Transportation Optimization

## 💼 Business use case

Waste operators must move large material volumes from generation centers to landfills while working within transfer-station capacities and transportation costs. At that scale, even small routing inefficiencies can become expensive, making the problem a strong candidate for mathematical optimization.

## 🎯 Principal objective

Minimize total transportation cost across two generation centers, four transfer depots, and six landfills (adding two more in the next two years) while satisfying supply, throughput, flow-conservation, and landfill-demand constraints. The formulation allows both direct shipments and routes through intermediate depots.

## 🔎 Summary of takeaways

The stored Gurobi solution is optimal at a total transportation cost of **\$541,000** for the scenario of six landfills, **\$617,000** for the scenario with seven landfills and **\$799,000** for the scenario with eight landfills. The resulting flow plan combines direct shipments with depot-based routing, showing how an optimization model can make both the total cost and the operational plan transparent.

The current formulation is deterministic, so its recommendations depend directly on the assumed costs, capacities, and demand. For operational use, I would add scenario analysis for demand uncertainty, lane disruptions, changing capacity, emissions, and service-failure penalties.

## 🧭 Explore the code

The [notebook](https://github.com/saels/landfill-network-optimization/blob/3ed851820266902d30c08344699a9e6d1e577d87/Landfill_network_optimization.ipynb) builds the network model from decision variables through constraints and objective function. Check the code to see how the optimal routing plan emerges from the business rules encoded in the optimization problem.
