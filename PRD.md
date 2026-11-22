# PRD: Campus Cafeteria Queue and Meal Management System

## 1. Project overview

The proposed Campus Cafeteria Queue and Meal Management System is a responsive web application intended to help students check meal availability before visiting the cafeteria and optionally reserve a meal. It will also help cafeteria management publish menus, record meal quantities and manage reservations.

The system is intended to reduce avoidable waiting and help students make informed meal choices. It will work alongside the cafeteria's existing process rather than replace the current meal entitlement or entrance arrangements.

## 2. The problem

**Main problem:** Students experience long and sometimes unpredictable queues at the campus cafeteria, while having limited information about whether the meals they want are still available before they reach the serving point.

This creates several difficulties:
- Students may spend time waiting in a queue only to find that their preferred meal has run out.
- Students may have to choose a different meal at the last minute.
- Some students may leave without collecting food.
- Students who already know what they want before arriving cannot easily check availability in advance.

### Why this problem needs attention

Students need a way to make informed meal choices before joining a queue. Cafeteria management also needs a clear way to publish availability and manage any advance reservations without preventing other students from buying meals through the existing walk-in process.

### Proposed problem focus

The project will therefore focus on reducing uncertainty about meal availability and supporting a more organised collection process through:
- Up-to-date menu and meal availability information.
- Optional meal preferences and reservations.
- Clear collection windows and reservation expiry rules.
- Records of portions reserved and collected.

The system is intended to reduce uncertainty and make meal collection more organised. Its effectiveness will depend on accurate and timely updates to meal availability.

## 3. Research carried out

Initial research was gathered through a short questionnaire completed by **7 students**. The questions covered queue frequency, meal periods, unavailable preferred meals, what students do when a meal is unavailable, meal preferences and interest in an advance information or reservation system.

This is a small convenience sample. The findings provide early indications of student experiences; they should not be treated as representative of the entire university.

### 3.1 Survey findings

| Topic | Responses |
|---|---:|
| Queue frequency | 5 often or sometimes; 1 rarely; 1 never |
| Meal period with the longest queues | 3 lunch; 1 dinner; 3 varies |
| Have experienced a preferred meal running out | 5 yes; 2 no |
| What they do if their preferred meal is unavailable | 5 choose another meal; 2 leave without collecting |
| Have ever left without collecting food | 5 yes; 2 no |
| Know what they want before arriving | 7 yes |
| Think advance meal information would be useful | 7 yes |
| Would use a preference/reservation system | 6 yes; 1 no |

Other comments included long queues, waiting outside, concerns about food quality, repeated meals, a desire for more variety, and the need for more organised spaces. Some respondents did not provide additional comments.

### 3.2 What the findings suggest

- Students may benefit from seeing menu and availability information before joining a queue.
- Meal reservations should be optional because one respondent was not interested in using such a system.
- Walk-in students must still be accommodated, subject to available food.
- Food variety, quality and cafeteria layout should be shared with the appropriate university or cafeteria personnel. They are outside the direct control of this software MVP.


## 4. Existing process and identified gaps

Based on the student information gathered so far:

- Students enter the cafeteria using the existing student identification/biometric process.
- Students choose from the meals available at the serving points.
- Students may only discover that a preferred meal has run out when they reach the serving area.
- Students may join queues without knowing the current availability of each meal.


## 5. Proposed solution

Build a responsive web application with two main user groups:

1. **Students:** View the day's menu and meal availability, indicate a preference, optionally reserve an available meal, cancel within the permitted time, and view reservation status.
2. **Cafeteria management:** Publish menus, enter meal quantities, update availability, set reservation and collection periods, and view reservation and collection records.

Students who do not want to reserve can continue using the existing walk-in process. The application will display availability information, but the accuracy of that information depends on timely updates by authorised staff.

## 6. Product goals

The system aims to:

- Give students earlier information about available meals.
- Reduce avoidable queues caused by uncertainty about meal availability.
- Allow interested students to reserve meals before arriving.
- Give management a clearer view of reservations and recorded collections.
- Preserve the existing cafeteria process for students who prefer to walk in.

## 7. Users and needs

### Students

Students need to:
- View the menu for the relevant meal period.
- See whether a meal is available, running low or sold out.
- Reserve a meal if they choose to.
- Change or cancel a reservation before the stated deadline.
- See the collection period and reservation status.
- Continue to use the walk-in option if they do not want to reserve.

### Cafeteria management

Authorised management users need to:
- Create and update daily menus.
- Enter the quantity prepared or made available for each meal.
- Set the number of portions available for reservation.
- View reservations and waiting-list requests.
- Record collections and update availability.
- Review basic reservation and collection information.


## 8. MVP scope

The Minimum Viable Product (MVP) will contain only the features needed to test whether advance meal information and optional reservations can improve the current process.

### Included in the MVP

- Student registration and sign-in.
- Basic student account verification, subject to an approved method.
- Daily menu display.
- Meal availability status: **Available**, **Running low** or **Sold out**.
- Optional meal preference indication.
- Optional reservation of available portions.
- Reservation confirmation and status.
- Cancellation or changes before a management-defined deadline.
- A collection window for confirmed reservations.
- Expiry of reservations that are not collected within the stated window.
- A waiting list when a meal's reservable portions are fully allocated.
- Management interface for menus, quantities, reservations and collection records.
- Basic records that allow management to compare portions prepared, reserved and collected.

### Not included in the MVP

- Online payment, because the existing meal entitlement is separate from this proposed reservation system.
- Replacement of the existing biometric entrance scanner.
- Automatic integration with university student databases or biometric systems.
- A dedicated Android or iOS application.
- Automated demand prediction or advanced analytics.
- Direct management of food preparation, food quality or menu variety.


## 9. Main user workflows

### Student workflow

1. The student signs in.
2. The student selects the relevant meal period.
3. The student views the menu and availability.
4. The student either walks in as usual or selects a meal to reserve.
5. If portions are available, the system confirms the reservation and displays the collection window.
6. The student collects the meal within the stated period.
7. The reservation is marked as collected. If the student does not arrive before expiry, the reservation expires according to the agreed policy.

### Management workflow

1. An authorised user signs in.
2. The user creates or updates the meal menu.
3. The user enters quantities and the portions available for reservation.
4. The user reviews reservations and waiting-list requests.
5. The user records collections and updates quantities when meals are served.
6. The system displays updated availability based on the records entered.

## 10. Functional requirements

| ID | Requirement |
|---|---|
| FR-01 | The system shall allow students to register and sign in. |
| FR-02 | The system shall provide access only to authorised management users for management functions. |
| FR-03 | Students shall be able to view menus by day and meal period. |
| FR-04 | Students shall be able to view the availability status of each listed meal. |
| FR-05 | Students shall be able to indicate a meal preference. |
| FR-06 | Students shall be able to reserve a meal when reservable portions are available. |
| FR-07 | The system shall confirm successful reservations and show their collection window. |
| FR-08 | Students shall be able to cancel or change reservations before the stated deadline, subject to availability. |
| FR-09 | The system shall place eligible students on a waiting list when reservable portions are fully allocated. |
| FR-10 | The system shall expire reservations that are not collected within the stated collection window. |
| FR-11 | Authorised management users shall be able to create and update menus and meal quantities. |
| FR-12 | Authorised management users shall be able to view reservations and record collections. |
| FR-13 | The system shall update displayed availability when management records a relevant quantity or collection change. |

## 11. Non-functional requirements

- **Usability:** The main student tasks should be simple to understand and complete.
- **Responsiveness:** The application should work on common mobile phones, tablets and computers.
- **Security:** User accounts and reservation records should be protected from unauthorised access.
- **Access control:** Students must not be able to use management functions.
- **Reliability:** The system should avoid confirming more reservations than the configured reservable quantity.
- **Data accuracy:** Availability should reflect the latest quantities entered and collections recorded by management.
- **Performance:** Menus and reservation information should load within a reasonable time under expected campus usage.
- **Maintainability:** The system should be organised so that future changes can be made without rebuilding the entire application.

## 12. Business rules

1. A student may choose not to use reservations and may continue as a walk-in.
2. A reservation is optional and does not replace the student's existing meal entitlement.
3. A reservation is confirmed only when a portion has been successfully allocated.
4. Reservations must not exceed the quantity made available for reservation.
5. If demand exceeds reservable portions, allocation should follow a fair first-come, first-served process.
6. A student whose selected meal is fully reserved may choose another available meal or join the waiting list.
7. Students may cancel or change reservations only before the configured deadline and where availability permits.
8. A reservation expires if it is not collected within its collection window.
9. When a reservation expires, the portion may be offered to the next eligible student on the waiting list or returned to general availability.
10. Management is responsible for entering accurate menu and quantity information.

## 13. Meal quantity and reservation handling

The system must distinguish between portions prepared, portions reserved, portions collected and portions still available to walk-in students. This is necessary to avoid allocating the same portion more than once.

For example, if 200 portions are recorded, 40 have been collected and 60 are reserved, then 100 portions remain unreserved.

The system should not automatically assume that every portion prepared is available for reservation. Management should be able to decide how many portions are reserved for advance collection and how many remain for walk-in students.

## 14. Success measures

The team can evaluate the MVP using:

- Average student waiting time.
- Queue length during busy meal periods.
- Number of times a listed meal becomes unavailable earlier than expected.
- Percentage of confirmed reservations collected.
- Number of expired or missed reservations.
- Accuracy of recorded meal quantities.
- Student feedback on the usefulness of availability information.

Waiting time and queue length can be compared before and after the system is introduced.

## 15. Assumptions, constraints and risks

### Assumptions and constraints

- Students have access to internet-enabled devices.
- Authorised cafeteria staff will enter menus and update meal quantities.
- Student account verification will use an approved method.
- The MVP depends on accurate and timely updates from staff.
- Internet access is required to use the web application.
- The existing biometric entrance process will remain unchanged.

### Risks and possible responses

| Risk | Possible response |
|---|---|
| Quantities are not updated promptly | Agree who is responsible for updates and when they must be made. |
| Students reserve meals but do not collect them | Use a clear collection window and expiry policy. |
| Reservations reduce food available to walk-in students | Let management control the number of reservable portions. |
| Students do not adopt the system | Keep reservations optional and retain walk-in service. |
| Internet access is unreliable | Keep the existing cafeteria process available as a fallback. |
| Student account verification is difficult | Confirm an approved verification method before implementation. |

## 16. Future improvements

If the MVP is successful, later versions may consider integration with approved university records, improved demand reports, demand forecasting, a dedicated mobile application, and possible integration with existing campus systems. These features are not required for the first version.

## 17. Conclusion

The proposed system addresses a practical student concern: uncertainty about meal availability and the time spent waiting for food. Initial responses from seven students suggest that queues and unavailable preferred meals affect several respondents, while all seven said advance meal information would be useful. Six said they would use a preference or reservation system, so the system should remain optional.

The MVP can be evaluated using waiting-time, availability and collection records, together with student feedback.
