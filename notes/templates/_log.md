<% _.each(pulls, function(issue) {
%>- [#<%= issue.number %>](<%= issue.html_url %>) - <%= issue.title %> ([@<%= issue.user.login %>](<%= issue.user.url %>))
<%
}); 
_.each(issues, function(issue) {
%>- [#<%= issue.number %>](<%= issue.html_url %>) - <%= issue.title %>
<%
});
_.each(commits, function(commit) {
%>- <%= commit.title %> - <%= commit.sha %>
<%
});

if (links.length) {
%>
Referenced Links:<%

_.each(links, function(link) { %>
- [<%= link.title %>](<%= link.url %>)<%
});
} %>
Compatibility notes:
- TODO : What might have broken?
