---
title: Module managementgroups
aliases:
    - "/reference/pkg/nodejs/@pulumi/azure/managementgroups/"
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/azure</a> &gt; managementgroups

<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#ManagementGroup">class ManagementGroup</a></li>
<li><a href="#getManagementGroup">function getManagementGroup</a></li>
<li><a href="#GetManagementGroupArgs">interface GetManagementGroupArgs</a></li>
<li><a href="#GetManagementGroupResult">interface GetManagementGroupResult</a></li>
<li><a href="#ManagementGroupArgs">interface ManagementGroupArgs</a></li>
<li><a href="#ManagementGroupState">interface ManagementGroupState</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts">managementgroups/getManagementGroup.ts</a> <a href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts">managementgroups/managementGroup.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="ManagementGroup">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L28">class <b>ManagementGroup</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>

Manages a Management Group.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const current = pulumi.output(azure.core.getSubscription({}));
const exampleParent = new azure.managementgroups.ManagementGroup("example_parent", {
    displayName: "ParentGroup",
    subscriptionIds: [current.subscriptionId],
});
const exampleChild = new azure.managementgroups.ManagementGroup("example_child", {
    displayName: "ChildGroup",
    parentManagementGroupId: exampleParent.id,
    subscriptionIds: [current.subscriptionId],
});
```

<h3 class="pdoc-member-header" id="ManagementGroup-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L56"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> ManagementGroup(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args?: <a href='#ManagementGroupArgs'>ManagementGroupArgs</a>, opts?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>


Create a ManagementGroup resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L37">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#ManagementGroupState'>ManagementGroupState</a>, opts?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#ManagementGroup'>ManagementGroup</a></pre>


Get an existing ManagementGroup resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L14">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L107">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L44">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>displayName: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

A friendly name for this Management Group. If not specified, this'll be the same as the `group_id`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L48">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>groupId: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The UUID for this Management Group, which needs to be unique across your tenant - which will be generated if not provided. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L102">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-parentManagementGroupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L52">property <b>parentManagementGroupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>parentManagementGroupId: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the Parent Management Group. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-subscriptionIds">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L56">property <b>subscriptionIds</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>subscriptionIds: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

A list of Subscription GUIDs which should be assigned to the Management Group.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroup-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="getManagementGroup">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L23">function <b>getManagementGroup</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span>getManagementGroup(args: <a href='#GetManagementGroupArgs'>GetManagementGroupArgs</a>, opts?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions'>pulumi.InvokeOptions</a>): <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise'>Promise</a>&lt;<a href='#GetManagementGroupResult'>GetManagementGroupResult</a>&gt;</pre>


Use this data source to access information about an existing Management Group.

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as azure from "@pulumi/azure";

const test = pulumi.output(azure.managementgroups.getManagementGroup({
    groupId: "00000000-0000-0000-0000-000000000000",
}));

export const displayName = test.displayName;
```

{{% /md %}}
</div>
<h2 class="pdoc-module-header" id="GetManagementGroupArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L39">interface <b>GetManagementGroupArgs</b></a>
</h2>
<div class="pdoc-module-contents">

A collection of arguments for invoking getManagementGroup.

<h3 class="pdoc-member-header" id="GetManagementGroupArgs-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L43">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

Specifies the UUID of this Management Group.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="GetManagementGroupResult">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L49">interface <b>GetManagementGroupResult</b></a>
</h2>
<div class="pdoc-module-contents">

A collection of values returned by getManagementGroup.

<h3 class="pdoc-member-header" id="GetManagementGroupResult-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L53">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>displayName: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

A friendly name for the Management Group.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetManagementGroupResult-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L54">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}
{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetManagementGroupResult-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L66">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetManagementGroupResult-parentManagementGroupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L58">property <b>parentManagementGroupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>parentManagementGroupId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;</pre>
{{% md %}}

The ID of any Parent Management Group.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="GetManagementGroupResult-subscriptionIds">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/getManagementGroup.ts#L62">property <b>subscriptionIds</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>subscriptionIds: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[];</pre>
{{% md %}}

A list of Subscription ID's which are assigned to the Management Group.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="ManagementGroupArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L117">interface <b>ManagementGroupArgs</b></a>
</h2>
<div class="pdoc-module-contents">

The set of arguments for constructing a ManagementGroup resource.

<h3 class="pdoc-member-header" id="ManagementGroupArgs-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L121">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>displayName?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

A friendly name for this Management Group. If not specified, this'll be the same as the `group_id`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupArgs-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L125">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupId?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The UUID for this Management Group, which needs to be unique across your tenant - which will be generated if not provided. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupArgs-parentManagementGroupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L129">property <b>parentManagementGroupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>parentManagementGroupId?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the Parent Management Group. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupArgs-subscriptionIds">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L133">property <b>subscriptionIds</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>subscriptionIds?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

A list of Subscription GUIDs which should be assigned to the Management Group.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="ManagementGroupState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L95">interface <b>ManagementGroupState</b></a>
</h2>
<div class="pdoc-module-contents">

Input properties used for looking up and filtering ManagementGroup resources.

<h3 class="pdoc-member-header" id="ManagementGroupState-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L99">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>displayName?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

A friendly name for this Management Group. If not specified, this'll be the same as the `group_id`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupState-groupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L103">property <b>groupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>groupId?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The UUID for this Management Group, which needs to be unique across your tenant - which will be generated if not provided. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupState-parentManagementGroupId">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L107">property <b>parentManagementGroupId</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>parentManagementGroupId?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the Parent Management Group. Changing this forces a new resource to be created.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="ManagementGroupState-subscriptionIds">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-azure/blob/9ad002cd8d3c86adcf7430e550cbb381cb2e36c5/sdk/nodejs/managementgroups/managementGroup.ts#L111">property <b>subscriptionIds</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>subscriptionIds?: <a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

A list of Subscription GUIDs which should be assigned to the Management Group.

{{% /md %}}
</div>
</div>