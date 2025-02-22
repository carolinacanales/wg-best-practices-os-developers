# GitHub Configuration Best Practices

## Intro

GitHub is a collaborative source code management platform that plays a critical role in modern software development, providing a central repository for storing, managing, and versioning source code as well as collaborating with a community of developers. However, it also represent a potential security risk if not properly configured. In this guide, we will explore the best practices for securing GitHub, covering topics that include user authentication, access control, permissions, monitoring, logging, and integrating security tools.

## Audience

This guide has been written for the:

* **Maintainer** who wants to improve the security posture for one or more GitHub repositories they support.  
* **Open Source Program Office (OSPO)** who is typically responsible for multiple organizations and repositories.
* **Operations** team tasked with applying policies as part of their work managing assets on GitHub.

## Recommendations

### Continuous Integration / Continuous Deployment
1. [Workflows Should Not Be Allowed To Approve Pull Requests](actions/actions_can_approve_pull_requests.md)
2. [GitHub Actions Should Be Restricted To Selected Repositories](actions/all_repositories_can_run_github_actions.md)
3. [GitHub Actions Should Be Limited To Verified or Explicitly Trusted Actions](actions/all_github_actions_are_allowed.md)
4. [Default Workflow Token Permission Should Be Read Only](actions/token_default_permissions_is_read_write.md)
### Server
1. [Two-Factor Authentication Should Be Enforced For The Enterprise](enterprise/enterprise_enforce_two_factor_authentication.md)
2. [Enterprise Should Not Allow Members To Create public Repositories](enterprise/enterprise_allows_creating_public_repos.md)
3. [Enterprise Should Not Allow Members To Invite Outside Collaborators](enterprise/enterprise_allows_inviting_externals_collaborators.md)
4. [Enterprise Should Not Allow Members To Change Repository Visibility](enterprise/enterprise_not_using_visibility_change_disable_policy.md)
5. [Enterprise Should Use Single-Sign-On](enterprise/enterprise_not_using_single_sign_on.md)
6. [Enterprise Should Not Allow Members To Fork Internal And Private Repositories](enterprise/enterprise_allows_forking_repos.md)
### Members, Access Control and Permissions
1. [Organization Should Have Fewer Than Three Owners](member/organization_has_too_many_admins.md)
2. [Organization Admins Should Have Activity In The Last 6 Months](member/stale_admin_found.md)
3. [Organization Members Should Have Activity In The Last 6 Months](member/stale_member_found.md)
### Organizational Management
1. [Two-Factor Authentication Should Be Enforced For The Organization](organization/two_factor_authentication_not_required_for_org.md)
2. [Default Member Permissions Should Be Restricted](organization/default_repository_permission_is_not_none.md)
3. [Only Admins Should Be Able To Create Public Repositories](organization/non_admins_can_create_public_repositories.md)
4. [Organization Should Use Single-Sign-On](organization/organization_not_using_single_sign_on.md)
5. [Webhooks Should Be Configured To Use SSL](organization/organization_webhook_doesnt_require_ssl.md)
6. [Webhooks Should Be Configured With A Secret](organization/organization_webhook_no_secret.md)
### Repository configuration
1. [Repository Should Be Updated At Least Quarterly](repository/repository_not_maintained.md)
2. [Workflows Should Not Be Allowed To Approve Pull Requests](repository/actions_can_approve_pull_requests.md)
3. [Default Branch Should Require Code Review](repository/code_review_not_required.md)
4. [Default Workflow Token Permission Should Be Set To Read Only](repository/token_default_permissions_is_read_write.md)
5. [Default Branch Should Be Protected](repository/missing_default_branch_protection.md)
6. [Default Branch Should Not Allow Force Pushes](repository/missing_default_branch_protection_force_push.md)
7. [Default Branch Should Require Code Review By At Least Two Reviewers](repository/code_review_by_two_members_not_required.md)
8. [Vulnerability Alerts Should Be Enabled](repository/vulnerability_alerts_not_enabled.md)
9. [OSSF Scorecard Score Should Be Above 7](repository/scorecard_score_too_low.md)
10. [GitHub Advanced Security – Dependency Review Should Be Enabled For A Repository](repository/ghas_dependency_review_not_enabled.md)
11. [Default Branch Deletion Protection Should Be Enabled](repository/missing_default_branch_protection_deletion.md)
12. [Default Branch Should Require Linear History](repository/non_linear_history.md)
13. [Default Branch Should Require All Checks To Pass Before Merge](repository/requires_status_checks.md)
14. [Default Branch Should Require Branches To Be Up To Date Before Merge](repository/requires_branches_up_to_date_before_merge.md)
15. [Repository Should Have Fewer Than Three Admins](repository/repository_has_too_many_admins.md)
16. [Default Branch Should Restrict Who Can Push To It](repository/pushes_are_not_restricted.md)
17. [Default Branch Should Require All Commits To Be Signed](repository/no_signed_commits.md)
18. [Webhooks Should Be Configured With A Secret](repository/repository_webhook_no_secret.md)
19. [Webhooks Should Be Configured To Use SSL](repository/repository_webhook_doesnt_require_ssl.md)
20. [Default Branch Should Require All Conversations To Be Resolved Before Merge](repository/no_conversation_resolution.md)
21. [Default Branch Should Restrict Who Can Dismiss Reviews](repository/review_dismissal_allowed.md)
22. [Default Branch Should Require New Code Changes After Approval To Be Re-Approved](repository/dismisses_stale_reviews.md)
23. [Default Branch Should Limit Code Review to Code-Owners](repository/code_review_not_limited_to_code_owners.md)
24. [Forking Should Not Be Allowed for This Repository](repository/forking_allowed_for_repository.md)
### Continuous Integration / Continuous Deployment
1. [Runner Group Should Be Limited to Private Repositories](runner_group/runner_group_can_be_used_by_public_repositories.md)
2. [Runner Group Should Be Limited to Selected Repositories](runner_group/runner_group_not_limited_to_selected_repositories.md)

### Operations

General Recommendations
- Organization Management Should Be Consolidated Under a Central Account.
- Organization Membership Should Be Limited to Employees.
- Review Security Policies and Procedures At Least Annually.
- Establish a Clear Communication and Incident Response Plan.
- Conduct Regular Security Audits and Vulnerability Assessments.
- Use Insights to Track Activity and in Repositories and Organizations.
- Use Tools Built On APIs to Automate Tasks and Avoid Needing Elevated Privileges.
- Provide Automated Alerts and Tooling to Ensure Ongoing Compliance.
- Review Audit Logs to Track Activity and Changes in Repositories and Organizations.
- Review Audit Events to Track Activity and Changes in Projects and Groups.

Specific Recommendations
- [Two-Factor Authentication Should Be Enforced For The Organization](organization/two_factor_authentication_not_required_for_org.md)
- [Organization Should Use Single-Sign-On](organization/organization_not_using_single_sign_on.md)
- [Default Member Permissions Should Be Restricted](organization/default_repository_permission_is_not_none.md)
- [Only Admins Should Be Able To Create Public Repositories](organization/non_admins_can_create_public_repositories.md)
- [Webhooks Should Be Configured To Use SSL](organization/organization_webhook_doesnt_require_ssl.md)
- [Webhooks Should Be Configured With A Secret](organization/organization_webhook_no_secret.md)
- Configure Security Alerts and Vulnerability Scanning at the Organization or Repository Level.
- Enable GitHub Advanced Security features for Private and Internal Repositories.
