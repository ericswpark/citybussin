# citybussin

WIP, will eat your underfunded bus

CityBus (of West Lafayette)'s API wrapped up in a Python library


# Usage

Import library and use


## Example

```python
from citybussin import Citybussin
c = Citybussin()

target_route = c.get_route_by_short_name("4B")
# {'key': '7de23591-ec36-4ba9-bc17-ccafeafb95c4', 'name': 'Purdue West', 'shortName': '4B', 'directionList': [{'direction': {'key': '191819d0-9173-4a89-855f-2e1e42decae1', 'name': 'to CityBus Center'}, 'destination': 'to Campus & CityBus Center', 'lineColor': '#007F49', 'textColor': '#FFFFFF', 'patternList': [{'key': 'cf0c64a3-7b5e-4c68-a012-2029aed9d7f8', 'isDisplay': True}], 'serviceInterruptionKeys': [3274]}, {'direction': {'key': '91801df8-8e37-44e2-8029-0662a713a619', 'name': 'to WL Walmart'}, 'destination': 'to Campus & WL Walmart', 'lineColor': '#007F49', 'textColor': '#FFFFFF', 'patternList': [{'key': 'b7e2e890-98a4-421c-8917-683467c8db03', 'isDisplay': True}], 'serviceInterruptionKeys': []}]}
target_route_stops = c.get_route_stops(target_route["key"])
# [{'name': 'Walmart West Lafayette (at Shelter): BUS403', 'stopCode': 'BUS403', 'stopType': 0}, {'name': 'Slim Chickens-Cumberland Ave (SE Corner):  BUS922', 'stopCode': 'BUS922', 'stopType': 0}, {'name': 'Northwestern Ave & Neil Armstrong Dr (NW): BUS162', 'stopCode': 'BUS162', 'stopType': 0}, {'name': 'Northwestern Ave & Yeager Rd (NW Corner): BUS161', 'stopCode': 'BUS161', 'stopType': 0}, {'name': 'Northwestern Ave & Windsor DR: BUS897', 'stopCode': 'BUS897', 'stopType': 0}, {'name': 'Northwestern Ave & Lindberg Rd: BUS375W', 'stopCode': 'BUS375W', 'stopType': 0}, {'name': 'Lindberg Rd & Kestral Blvd (NE Corner): BUS205', 'stopCode': 'BUS205', 'stopType': 0}, {'name': 'Village West Apts on Lindberg (at Shelter): BUS308', 'stopCode': 'BUS308', 'stopType': 0}, {'name': 'Station 21 on Lindberg (@ Shelter): BUS300', 'stopCode': 'BUS300', 'stopType': 0}, {'name': 'Blackbird Farms 2 on McCormick Rd: BUS304', 'stopCode': 'BUS304', 'stopType': 0}, {'name': 'SW Blackbird Farms Apt Buildings (W): BUS394', 'stopCode': 'BUS394', 'stopType': 0}, {'name': 'Schwartz Tennis Cntr on McCormick Rd: BUS906W', 'stopCode': 'BUS906W', 'stopType': 0}, {'name': 'McCormick Rd & Stadium Ave (NW Corner): BUS251W', 'stopCode': 'BUS251W', 'stopType': 0}, {'name': 'McCormick Rd & 3rd St: BUS501', 'stopCode': 'BUS501', 'stopType': 0}, {'name': 'Purdue West on Mitch Daniels Blvd (South): BUS566S', 'stopCode': 'BUS566S', 'stopType': 0}, {'name': 'Aspire Apts at Discovery Park: BUS011', 'stopCode': 'BUS011', 'stopType': 0}, {'name': 'Lilly Hall on Mitch Daniels Blvd (shelter): BUS345', 'stopCode': 'BUS345', 'stopType': 0}, {'name': 'Krannert Grad School: BUS260', 'stopCode': 'BUS260', 'stopType': 0}, {'name': 'Wabash Landing on State St (at Roebuck Dr): BUS644', 'stopCode': 'BUS644', 'stopType': 0}, {'name': 'CityBus Center: BUS215', 'stopCode': 'BUS215', 'stopType': 0}, {'name': 'CityBus Center: BUS215', 'stopCode': 'BUS215', 'stopType': 0}, {'name': 'Columbia St & 2nd St (NE Corner): BUS287NE', 'stopCode': 'BUS287NE', 'stopType': 0}, {'name': 'Wabash Landing on State St (at shelter): BUS156', 'stopCode': 'BUS156', 'stopType': 0}, {'name': 'Purdue Memorial Union (PMU) on MD Blvd: BUS271', 'stopCode': 'BUS271', 'stopType': 0}, {'name': 'Mitch Daniels Blv & Russell St (NE Corner): BUS547', 'stopCode': 'BUS547', 'stopType': 0}, {'name': 'First Street Towers on Mitch Daniels Blvd: BUS898', 'stopCode': 'BUS898', 'stopType': 0}, {'name': 'Purdue West on Mitch Daniels Blvd: BUS566', 'stopCode': 'BUS566', 'stopType': 0}, {'name': 'Purdue West on McCormick Rd: BUS504', 'stopCode': 'BUS504', 'stopType': 0}, {'name': 'McCormick Rd & Stadium Ave (NE Corner): BUS251E', 'stopCode': 'BUS251E', 'stopType': 0}, {'name': 'Schwartz Tennis Cntr on McCormick Rd: BUS906E', 'stopCode': 'BUS906E', 'stopType': 0}, {'name': 'SW Blackbird Farms Apt Buildings (E): BUS393', 'stopCode': 'BUS393', 'stopType': 0}, {'name': 'McCormick Rd & Lindberg Rd (SE Corner): BUS236', 'stopCode': 'BUS236', 'stopType': 0}, {'name': 'University Pl (at clubhouse): BUS551', 'stopCode': 'BUS551', 'stopType': 0}, {'name': 'Village West Apts on Lindberg (at Shelter): BUS308', 'stopCode': 'BUS308', 'stopType': 0}, {'name': 'Station 21 on Lindberg (@ Shelter): BUS300', 'stopCode': 'BUS300', 'stopType': 0}, {'name': 'Connection Point Church: BUS225', 'stopCode': 'BUS225', 'stopType': 0}, {'name': 'Lodge Apts on Cumberland Ave (@Shelter): BUS223', 'stopCode': 'BUS223', 'stopType': 0}, {'name': 'Walmart West Lafayette (at Shelter): BUS403', 'stopCode': 'BUS403', 'stopType': 0}]
target_route_directions = c.get_route_directions(target_route["key"])
# [{'direction': {'key': '191819d0-9173-4a89-855f-2e1e42decae1', 'name': 'to CityBus Center'}, 'destination': 'to Campus & CityBus Center', 'lineColor': '#007F49', 'textColor': '#FFFFFF', 'patternList': [{'key': 'cf0c64a3-7b5e-4c68-a012-2029aed9d7f8', 'isDisplay': True}], 'serviceInterruptionKeys': [3274]}, {'direction': {'key': '91801df8-8e37-44e2-8029-0662a713a619', 'name': 'to WL Walmart'}, 'destination': 'to Campus & WL Walmart', 'lineColor': '#007F49', 'textColor': '#FFFFFF', 'patternList': [{'key': 'b7e2e890-98a4-421c-8917-683467c8db03', 'isDisplay': True}], 'serviceInterruptionKeys': []}]
target_route_direction = target_route_directions[0]
# {'direction': {'key': '191819d0-9173-4a89-855f-2e1e42decae1', 'name': 'to CityBus Center'}, 'destination': 'to Campus & CityBus Center', 'lineColor': '#007F49', 'textColor': '#FFFFFF', 'patternList': [{'key': 'cf0c64a3-7b5e-4c68-a012-2029aed9d7f8', 'isDisplay': True}], 'serviceInterruptionKeys': [3274]}
next_depart_times = c.get_next_depart_times(target_route["key"], target_route_direction["direction"]["key"],
                                            target_route_stops[0]["stopCode"])
# [{'estimatedDepartTimeUtc': '2024-10-26T00:29:00Z', 'scheduledDepartTimeUtc': '2024-10-26T00:14:00Z', 'isOffRoute': False}, {'estimatedDepartTimeUtc': '2024-10-26T00:46:00Z', 'scheduledDepartTimeUtc': '2024-10-26T00:44:00Z', 'isOffRoute': False}, {'estimatedDepartTimeUtc': '2024-10-26T01:14:00Z', 'scheduledDepartTimeUtc': '2024-10-26T01:14:00Z', 'isOffRoute': False}]

import humanize
from datetime import datetime

humanize.naturaltime(datetime.fromisoformat(next_depart_times[0]["estimatedDepartTimeUtc"]))
# 14 minutes from now
```