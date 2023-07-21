---
title: "CollectionService"
weight: 10
date: 2023-07-21T07:17:01.692Z
showtoc: true
generated: true
---
<!-- This file was generated from the Vendure source. Do not modify. Instead, re-run the "docs:build" script -->
import MemberInfo from '@site/src/components/MemberInfo';
import GenerationInfo from '@site/src/components/GenerationInfo';
import MemberDescription from '@site/src/components/MemberDescription';


## CollectionService

<GenerationInfo sourceFile="packages/core/src/service/services/collection.service.ts" sourceLine="66" packageName="@vendure/core" />

Contains methods relating to <a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a> entities.

```ts title="Signature"
class CollectionService implements OnModuleInit {
  constructor(connection: TransactionalConnection, channelService: ChannelService, assetService: AssetService, facetValueService: FacetValueService, listQueryBuilder: ListQueryBuilder, translatableSaver: TranslatableSaver, eventBus: EventBus, jobQueueService: JobQueueService, configService: ConfigService, slugValidator: SlugValidator, configArgService: ConfigArgService, customFieldRelationService: CustomFieldRelationService, translator: TranslatorService, roleService: RoleService)
  async findAll(ctx: RequestContext, options?: ListQueryOptions<Collection> & { topLevelOnly?: boolean }, relations?: RelationPaths<Collection>) => Promise<PaginatedList<Translated<Collection>>>;
  async findOne(ctx: RequestContext, collectionId: ID, relations?: RelationPaths<Collection>) => Promise<Translated<Collection> | undefined>;
  async findByIds(ctx: RequestContext, ids: ID[], relations?: RelationPaths<Collection>) => Promise<Array<Translated<Collection>>>;
  async findOneBySlug(ctx: RequestContext, slug: string, relations?: RelationPaths<Collection>) => Promise<Translated<Collection> | undefined>;
  getAvailableFilters(ctx: RequestContext) => ConfigurableOperationDefinition[];
  async getParent(ctx: RequestContext, collectionId: ID) => Promise<Collection | undefined>;
  async getChildren(ctx: RequestContext, collectionId: ID) => Promise<Collection[]>;
  async getBreadcrumbs(ctx: RequestContext, collection: Collection) => Promise<Array<{ name: string; id: ID }>>;
  async getCollectionsByProductId(ctx: RequestContext, productId: ID, publicOnly: boolean) => Promise<Array<Translated<Collection>>>;
  async getDescendants(ctx: RequestContext, rootId: ID, maxDepth: number = Number.MAX_SAFE_INTEGER) => Promise<Array<Translated<Collection>>>;
  getAncestors(collectionId: ID) => Promise<Collection[]>;
  getAncestors(collectionId: ID, ctx: RequestContext) => Promise<Array<Translated<Collection>>>;
  async getAncestors(collectionId: ID, ctx?: RequestContext) => Promise<Array<Translated<Collection> | Collection>>;
  async previewCollectionVariants(ctx: RequestContext, input: PreviewCollectionVariantsInput, options?: ListQueryOptions<ProductVariant>, relations?: RelationPaths<Collection>) => Promise<PaginatedList<ProductVariant>>;
  async create(ctx: RequestContext, input: CreateCollectionInput) => Promise<Translated<Collection>>;
  async update(ctx: RequestContext, input: UpdateCollectionInput) => Promise<Translated<Collection>>;
  async delete(ctx: RequestContext, id: ID) => Promise<DeletionResponse>;
  async move(ctx: RequestContext, input: MoveCollectionInput) => Promise<Translated<Collection>>;
  async getCollectionProductVariantIds(collection: Collection, ctx?: RequestContext) => Promise<ID[]>;
  async assignCollectionsToChannel(ctx: RequestContext, input: AssignCollectionsToChannelInput) => Promise<Array<Translated<Collection>>>;
  async removeCollectionsFromChannel(ctx: RequestContext, input: RemoveCollectionsFromChannelInput) => Promise<Array<Translated<Collection>>>;
}
```
* Implements: <code>OnModuleInit</code>



<div className="members-wrapper">

### constructor

<MemberInfo kind="method" type="(connection: <a href='/docs/reference/typescript-api/data-access/transactional-connection#transactionalconnection'>TransactionalConnection</a>, channelService: <a href='/docs/reference/typescript-api/services/channel-service#channelservice'>ChannelService</a>, assetService: <a href='/docs/reference/typescript-api/services/asset-service#assetservice'>AssetService</a>, facetValueService: <a href='/docs/reference/typescript-api/services/facet-value-service#facetvalueservice'>FacetValueService</a>, listQueryBuilder: <a href='/docs/reference/typescript-api/data-access/list-query-builder#listquerybuilder'>ListQueryBuilder</a>, translatableSaver: <a href='/docs/reference/typescript-api/service-helpers/translatable-saver#translatablesaver'>TranslatableSaver</a>, eventBus: <a href='/docs/reference/typescript-api/events/event-bus#eventbus'>EventBus</a>, jobQueueService: <a href='/docs/reference/typescript-api/job-queue/job-queue-service#jobqueueservice'>JobQueueService</a>, configService: ConfigService, slugValidator: <a href='/docs/reference/typescript-api/service-helpers/slug-validator#slugvalidator'>SlugValidator</a>, configArgService: ConfigArgService, customFieldRelationService: CustomFieldRelationService, translator: TranslatorService, roleService: <a href='/docs/reference/typescript-api/services/role-service#roleservice'>RoleService</a>) => CollectionService"   />


### findAll

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, options?: ListQueryOptions&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62; &#38; { topLevelOnly?: boolean }, relations?: RelationPaths&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;) => Promise&#60;<a href='/docs/reference/typescript-api/common/paginated-list#paginatedlist'>PaginatedList</a>&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />


### findOne

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>, relations?: RelationPaths&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;) => Promise&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62; | undefined&#62;"   />


### findByIds

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, ids: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>[], relations?: RelationPaths&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />


### findOneBySlug

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, slug: string, relations?: RelationPaths&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;) => Promise&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62; | undefined&#62;"   />


### getAvailableFilters

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => ConfigurableOperationDefinition[]"   />

Returns all configured CollectionFilters, as specified by the <a href='/docs/reference/typescript-api/products-stock/catalog-options#catalogoptions'>CatalogOptions</a>.
### getParent

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>) => Promise&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a> | undefined&#62;"   />


### getChildren

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>) => Promise&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>[]&#62;"   />

Returns all child Collections of the Collection with the given id.
### getBreadcrumbs

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, collection: <a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>) => Promise&#60;Array&#60;{ name: string; id: <a href='/docs/reference/typescript-api/common/id#id'>ID</a> }&#62;&#62;"   />

Returns an array of name/id pairs representing all ancestor Collections up
to the Root Collection.
### getCollectionsByProductId

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, productId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>, publicOnly: boolean) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />

Returns all Collections which are associated with the given Product ID.
### getDescendants

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, rootId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>, maxDepth: number = Number.MAX_SAFE_INTEGER) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />

Returns the descendants of a Collection as a flat array. The depth of the traversal can be limited
with the maxDepth argument. So to get only the immediate children, set maxDepth = 1.
### getAncestors

<MemberInfo kind="method" type="(collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>) => Promise&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>[]&#62;"   />

Gets the ancestors of a given collection. Note that since ProductCategories are implemented as an adjacency list, this method
will produce more queries the deeper the collection is in the tree.
### getAncestors

<MemberInfo kind="method" type="(collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>, ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />


### getAncestors

<MemberInfo kind="method" type="(collectionId: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>, ctx?: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62; | <a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;"   />


### previewCollectionVariants

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: PreviewCollectionVariantsInput, options?: ListQueryOptions&#60;<a href='/docs/reference/typescript-api/entities/product-variant#productvariant'>ProductVariant</a>&#62;, relations?: RelationPaths&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;) => Promise&#60;<a href='/docs/reference/typescript-api/common/paginated-list#paginatedlist'>PaginatedList</a>&#60;<a href='/docs/reference/typescript-api/entities/product-variant#productvariant'>ProductVariant</a>&#62;&#62;"   />


### create

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: CreateCollectionInput) => Promise&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;"   />


### update

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: UpdateCollectionInput) => Promise&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;"   />


### delete

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, id: <a href='/docs/reference/typescript-api/common/id#id'>ID</a>) => Promise&#60;DeletionResponse&#62;"   />


### move

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: MoveCollectionInput) => Promise&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;"   />

Moves a Collection by specifying the parent Collection ID, and an index representing the order amongst
its siblings.
### getCollectionProductVariantIds

<MemberInfo kind="method" type="(collection: <a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>, ctx?: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>) => Promise&#60;<a href='/docs/reference/typescript-api/common/id#id'>ID</a>[]&#62;"   />


### assignCollectionsToChannel

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: AssignCollectionsToChannelInput) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />

Assigns Collections to the specified Channel
### removeCollectionsFromChannel

<MemberInfo kind="method" type="(ctx: <a href='/docs/reference/typescript-api/request/request-context#requestcontext'>RequestContext</a>, input: RemoveCollectionsFromChannelInput) => Promise&#60;Array&#60;Translated&#60;<a href='/docs/reference/typescript-api/entities/collection#collection'>Collection</a>&#62;&#62;&#62;"   />

Remove Collections from the specified Channel


</div>