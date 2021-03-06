---
title: Module bigtable
---

<!-- WARNING: this page was generated by a tool. Do not edit it by hand. -->
<!-- To change it, please see https://github.com/pulumi/docs/tree/master/tools/tscdocgen. -->

<a href="../">@pulumi/gcp</a> &gt; bigtable

> This provider is a derived work of the [Terraform Provider](https://github.com/terraform-providers/terraform-provider-gcp)
> distributed under [MPL 2.0](https://www.mozilla.org/en-US/MPL/2.0/). If you encounter a bug or missing feature,
> first check the [`pulumi/pulumi-gcp` repo](https://github.com/pulumi/pulumi-gcp/issues); however, if that doesn't turn up anything,
> please consult the source [`terraform-providers/terraform-provider-gcp` repo](https://github.com/terraform-providers/terraform-provider-gcp/issues).



<div class="toggleVisible">
<div class="collapsed">
<h2 class="pdoc-module-header toggleButton" title="Click to show Index">Index ▹</h2>
</div>
<div class="expanded">
<h2 class="pdoc-module-header toggleButton" title="Click to hide Index">Index ▾</h2>
<div class="pdoc-module-contents">
<ul>
<li><a href="#Instance">class Instance</a></li>
<li><a href="#Table">class Table</a></li>
<li><a href="#InstanceArgs">interface InstanceArgs</a></li>
<li><a href="#InstanceState">interface InstanceState</a></li>
<li><a href="#TableArgs">interface TableArgs</a></li>
<li><a href="#TableState">interface TableState</a></li>
</ul>

<a href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts">bigtable/instance.ts</a> <a href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts">bigtable/table.ts</a> 
</div>
</div>
</div>


<h2 class="pdoc-module-header" id="Instance">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L47">class <b>Instance</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

Creates a Google Bigtable instance. For more information see
[the official documentation](https://cloud.google.com/bigtable/) and
[API](https://cloud.google.com/bigtable/docs/go/reference).

## Example Usage - Production Instance

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gcp from "@pulumi/gcp";

const production_instance = new gcp.bigtable.Instance("production-instance", {
    clusters: [{
        clusterId: "tf-instance-cluster",
        numNodes: 3,
        storageType: "HDD",
        zone: "us-central1-b",
    }],
});
```

## Example Usage - Development Instance

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gcp from "@pulumi/gcp";

const development_instance = new gcp.bigtable.Instance("development-instance", {
    clusters: [{
        clusterId: "tf-instance-cluster",
        storageType: "HDD",
        zone: "us-central1-b",
    }],
    instanceType: "DEVELOPMENT",
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-google/blob/master/website/docs/r/bigtable_instance.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Instance-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L94"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Instance(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#InstanceArgs'>InstanceArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>


Create a Instance resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L56">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#InstanceState'>InstanceState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Instance'>Instance</a></pre>


Get an existing Instance resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L14">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L67">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>


Returns true if the given object is an instance of Instance.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-clusters">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L77">property <b>clusters</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>clusters: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{
    clusterId: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
    numNodes: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>;
    storageType: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
    zone: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
}[]&gt;;</pre>
{{% md %}}

A block of cluster configuration options. This can be specified 1 or 2 times. See structure below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L81">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>displayName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The human-readable display name of the Bigtable instance. Defaults to the instance `name`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L102">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-instanceType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L85">property <b>instanceType</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>instanceType: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span> | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

The instance type to create. One of `"DEVELOPMENT"` or `"PRODUCTION"`. Defaults to `"PRODUCTION"`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L89">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name (also called Instance Id in the Cloud Console) of the Cloud Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L94">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>project: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Instance-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="Table">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L37">class <b>Table</b></a>
</h2>
<div class="pdoc-module-contents">
<pre class="highlight"><span class='kd'>extends</span> <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResource'>CustomResource</a></pre>
{{% md %}}

Creates a Google Cloud Bigtable table inside an instance. For more information see
[the official documentation](https://cloud.google.com/bigtable/) and
[API](https://cloud.google.com/bigtable/docs/go/reference).

## Example Usage

```typescript
import * as pulumi from "@pulumi/pulumi";
import * as gcp from "@pulumi/gcp";

const instance = new gcp.bigtable.Instance("instance", {
    clusterId: "tf-instance-cluster",
    numNodes: 3,
    storageType: "HDD",
    zone: "us-central1-b",
});
const table = new gcp.bigtable.Table("table", {
    instanceName: instance.name,
    splitKeys: [
        "a",
        "b",
        "c",
    ],
});
```

> This content is derived from https://github.com/terraform-providers/terraform-provider-google/blob/master/website/docs/r/bigtable_table.html.markdown.

{{% /md %}}
<h3 class="pdoc-member-header" id="Table-constructor">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L84"> <b>constructor</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span><span class='kd'>new</span> Table(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, args: <a href='#TableArgs'>TableArgs</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>)</pre>


Create a Table resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-get">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L46">method <b>get</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>get(name: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>, id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>pulumi.ID</a>&gt;, state?: <a href='#TableState'>TableState</a>, opts?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions'>pulumi.CustomResourceOptions</a>): <a href='#Table'>Table</a></pre>


Get an existing Table resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-getProvider">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L14">method <b>getProvider</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'></span>getProvider(moduleMember: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>): ProviderResource | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span></pre>

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-isInstance">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L57">method <b>isInstance</b></a>
</h3>
<div class="pdoc-member-contents">
{{% md %}}

<pre class="highlight"><span class='kd'>public static </span>isInstance(obj: <span class='kd'><a href='https://www.typescriptlang.org/docs/handbook/basic-types.html#any'>any</a></span>): <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean'>boolean</a></span></pre>


Returns true if the given object is an instance of Table.  This is designed to work even
when multiple copies of the Pulumi SDK have been loaded into the same process.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-columnFamilies">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L67">property <b>columnFamilies</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>columnFamilies: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;{
    family: <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>;
}[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

A group of columns within a table which share a common configuration. This can be specified multiple times. Structure is documented below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-id">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L102">property <b>id</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>id: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#ID'>ID</a>&gt;;</pre>
{{% md %}}

id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-instanceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L71">property <b>instanceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>instanceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L75">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>name: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the table.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L80">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>project: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-splitKeys">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L84">property <b>splitKeys</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'>public </span>splitKeys: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>pulumi.Output</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>[] | <span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/undefined'>undefined</a></span>&gt;;</pre>
{{% md %}}

A list of predefined keys to split the table on.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="Table-urn">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">property <b>urn</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>urn: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Output'>Output</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#URN'>URN</a>&gt;;</pre>
{{% md %}}

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="InstanceArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L158">interface <b>InstanceArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Instance resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="InstanceArgs-clusters">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L162">property <b>clusters</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>clusters: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    clusterId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    numNodes: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;
    storageType: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    zone: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

A block of cluster configuration options. This can be specified 1 or 2 times. See structure below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceArgs-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L166">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>displayName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The human-readable display name of the Bigtable instance. Defaults to the instance `name`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceArgs-instanceType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L170">property <b>instanceType</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>instanceType?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The instance type to create. One of `"DEVELOPMENT"` or `"PRODUCTION"`. Defaults to `"PRODUCTION"`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L174">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name (also called Instance Id in the Cloud Console) of the Cloud Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceArgs-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L179">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="InstanceState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L131">interface <b>InstanceState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Instance resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="InstanceState-clusters">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L135">property <b>clusters</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>clusters?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    clusterId: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    numNodes: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number'>number</a></span>&gt;;
    storageType: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
    zone: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

A block of cluster configuration options. This can be specified 1 or 2 times. See structure below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceState-displayName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L139">property <b>displayName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>displayName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The human-readable display name of the Bigtable instance. Defaults to the instance `name`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceState-instanceType">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L143">property <b>instanceType</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>instanceType?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The instance type to create. One of `"DEVELOPMENT"` or `"PRODUCTION"`. Defaults to `"PRODUCTION"`.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L147">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name (also called Instance Id in the Cloud Console) of the Cloud Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="InstanceState-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/instance.ts#L152">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="TableArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L148">interface <b>TableArgs</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

The set of arguments for constructing a Table resource.

{{% /md %}}
<h3 class="pdoc-member-header" id="TableArgs-columnFamilies">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L152">property <b>columnFamilies</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>columnFamilies?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    family: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

A group of columns within a table which share a common configuration. This can be specified multiple times. Structure is documented below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableArgs-instanceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L156">property <b>instanceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>instanceName: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableArgs-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L160">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the table.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableArgs-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L165">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableArgs-splitKeys">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L169">property <b>splitKeys</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>splitKeys?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

A list of predefined keys to split the table on.

{{% /md %}}
</div>
</div>
<h2 class="pdoc-module-header" id="TableState">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L121">interface <b>TableState</b></a>
</h2>
<div class="pdoc-module-contents">
{{% md %}}

Input properties used for looking up and filtering Table resources.

{{% /md %}}
<h3 class="pdoc-member-header" id="TableState-columnFamilies">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L125">property <b>columnFamilies</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>columnFamilies?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;{
    family: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;
}&gt;[]&gt;;</pre>
{{% md %}}

A group of columns within a table which share a common configuration. This can be specified multiple times. Structure is documented below.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableState-instanceName">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L129">property <b>instanceName</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>instanceName?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the Bigtable instance.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableState-name">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L133">property <b>name</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>name?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The name of the table.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableState-project">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L138">property <b>project</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>project?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;;</pre>
{{% md %}}

The ID of the project in which the resource belongs. If it
is not provided, the provider project is used.

{{% /md %}}
</div>
<h3 class="pdoc-member-header" id="TableState-splitKeys">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-gcp/blob/6e7746d998f1196bccfd36a282c4fcd2ed4ace6a/sdk/nodejs/bigtable/table.ts#L142">property <b>splitKeys</b></a>
</h3>
<div class="pdoc-member-contents">
<pre class="highlight"><span class='kd'></span>splitKeys?: <a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<a href='/docs/reference/pkg/nodejs/pulumi/pulumi/#Input'>pulumi.Input</a>&lt;<span class='kd'><a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String'>string</a></span>&gt;[]&gt;;</pre>
{{% md %}}

A list of predefined keys to split the table on.

{{% /md %}}
</div>
</div>
