---
description: 'Más información acerca de: miembros de ColumnStream'
title: 'Miembros de ColumnStream '
TOCTitle: ColumnStream members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream_members(v=EXCHG.10)
ms:contentKeyID: 55101147
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9f35c0e000329bc98e2f9fd5873cd724516271d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571419"
---
# <a name="columnstream-members"></a><span data-ttu-id="81210-103">Miembros de ColumnStream </span><span class="sxs-lookup"><span data-stu-id="81210-103">ColumnStream members</span></span>

<span data-ttu-id="81210-104">Incluir miembros protegidos</span><span class="sxs-lookup"><span data-stu-id="81210-104">Include protected members</span></span>  
<span data-ttu-id="81210-105">Incluir miembros heredados</span><span class="sxs-lookup"><span data-stu-id="81210-105">Include inherited members</span></span>  

<span data-ttu-id="81210-106">Esta clase proporciona una interfaz de streaming a una columna de valor largo (es decir, una columna de tipo [LongBinary](./jet-coltyp-enumeration.md) o [LongText](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="81210-106">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="81210-107">El tipo [ColumnStream](./columnstream-class.md) expone los siguientes miembros.</span><span class="sxs-lookup"><span data-stu-id="81210-107">The [ColumnStream](./columnstream-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="81210-108">Constructores</span><span class="sxs-lookup"><span data-stu-id="81210-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="81210-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="81210-109">Name</span></span></th>
<th><span data-ttu-id="81210-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="81210-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span><span class="sxs-lookup"><span data-stu-id="81210-112"><a href="dn334142(v=exchg.10).md">ColumnStream</a></span></span></td>
<td><span data-ttu-id="81210-113">Inicializa una nueva instancia de la clase ColumnStream.</span><span class="sxs-lookup"><span data-stu-id="81210-113">Initializes a new instance of the ColumnStream class.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81210-114">Superior</span><span class="sxs-lookup"><span data-stu-id="81210-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="81210-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="81210-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="81210-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="81210-116">Name</span></span></th>
<th><span data-ttu-id="81210-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="81210-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span><span class="sxs-lookup"><span data-stu-id="81210-119"><a href="dn334201(v=exchg.10).md">CanRead</a></span></span></td>
<td><span data-ttu-id="81210-120">Obtiene un valor que indica si la secuencia admite lectura.</span><span class="sxs-lookup"><span data-stu-id="81210-120">Gets a value indicating whether the stream supports reading.</span></span> <span data-ttu-id="81210-121">(Invalida <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream. CanRead</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-121">(Overrides <a href="/dotnet/api/system.io.stream.canread#System_IO_Stream_CanRead">Stream.CanRead</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span><span class="sxs-lookup"><span data-stu-id="81210-123"><a href="dn334153(v=exchg.10).md">CanSeek</a></span></span></td>
<td><span data-ttu-id="81210-124">Obtiene un valor que indica si la secuencia admite operaciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="81210-124">Gets a value indicating whether the stream supports seeking.</span></span> <span data-ttu-id="81210-125">(Invalida <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream. CanSeek</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-125">(Overrides <a href="/dotnet/api/system.io.stream.canseek#System_IO_Stream_CanSeek">Stream.CanSeek</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span><span class="sxs-lookup"><span data-stu-id="81210-127"><a href="/dotnet/api/system.io.stream.cantimeout#System_IO_Stream_CanTimeout">CanTimeout</a></span></span></td>
<td><span data-ttu-id="81210-128">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-128">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span><span class="sxs-lookup"><span data-stu-id="81210-130"><a href="dn334204(v=exchg.10).md">CanWrite</a></span></span></td>
<td><span data-ttu-id="81210-131">Obtiene un valor que indica si la secuencia admite operaciones de escritura.</span><span class="sxs-lookup"><span data-stu-id="81210-131">Gets a value indicating whether the stream supports writing.</span></span> <span data-ttu-id="81210-132">(Invalida <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream. CanWrite</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-132">(Overrides <a href="/dotnet/api/system.io.stream.canwrite#System_IO_Stream_CanWrite">Stream.CanWrite</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-134"><a href="dn334159(v=exchg.10).md">Itag</a></span><span class="sxs-lookup"><span data-stu-id="81210-134"><a href="dn334159(v=exchg.10).md">Itag</a></span></span></td>
<td><span data-ttu-id="81210-135">Obtiene o establece el iTag de la columna.</span><span class="sxs-lookup"><span data-stu-id="81210-135">Gets or sets the itag of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-137"><a href="dn334205(v=exchg.10).md">Duración</a></span><span class="sxs-lookup"><span data-stu-id="81210-137"><a href="dn334205(v=exchg.10).md">Length</a></span></span></td>
<td><span data-ttu-id="81210-138">Obtiene la longitud actual de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="81210-138">Gets the current length of the stream.</span></span> <span data-ttu-id="81210-139">(Invalida <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream. length</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-139">(Overrides <a href="/dotnet/api/system.io.stream.length#System_IO_Stream_Length">Stream.Length</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-141"><a href="dn334161(v=exchg.10).md">Position</a></span><span class="sxs-lookup"><span data-stu-id="81210-141"><a href="dn334161(v=exchg.10).md">Position</a></span></span></td>
<td><span data-ttu-id="81210-142">Obtiene o establece la posición actual en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="81210-142">Gets or sets the current position in the stream.</span></span> <span data-ttu-id="81210-143">(Invalida <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream. Position</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-143">(Overrides <a href="/dotnet/api/system.io.stream.position#System_IO_Stream_Position">Stream.Position</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span><span class="sxs-lookup"><span data-stu-id="81210-145"><a href="/dotnet/api/system.io.stream.readtimeout#System_IO_Stream_ReadTimeout">ReadTimeout</a></span></span></td>
<td><span data-ttu-id="81210-146">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-146">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><span data-ttu-id="81210-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span><span class="sxs-lookup"><span data-stu-id="81210-148"><a href="/dotnet/api/system.io.stream.writetimeout#System_IO_Stream_WriteTimeout">WriteTimeout</a></span></span></td>
<td><span data-ttu-id="81210-149">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-149">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81210-150">Superior</span><span class="sxs-lookup"><span data-stu-id="81210-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="81210-151">Métodos</span><span class="sxs-lookup"><span data-stu-id="81210-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="81210-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="81210-152">Name</span></span></th>
<th><span data-ttu-id="81210-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="81210-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span><span class="sxs-lookup"><span data-stu-id="81210-155"><a href="/dotnet/api/system.io.stream.beginread#System_IO_Stream_BeginRead_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginRead</a></span></span></td>
<td><span data-ttu-id="81210-156">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-156">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span><span class="sxs-lookup"><span data-stu-id="81210-158"><a href="/dotnet/api/system.io.stream.beginwrite#System_IO_Stream_BeginWrite_System_Byte___System_Int32_System_Int32_System_AsyncCallback_System_Object_">BeginWrite</a></span></span></td>
<td><span data-ttu-id="81210-159">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-159">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Cerrar</a></span><span class="sxs-lookup"><span data-stu-id="81210-161"><a href="/dotnet/api/system.io.stream.close#System_IO_Stream_Close">Close</a></span></span></td>
<td><span data-ttu-id="81210-162">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-162">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span><span class="sxs-lookup"><span data-stu-id="81210-164"><a href="/dotnet/api/system.marshalbyrefobject.createobjref#System_MarshalByRefObject_CreateObjRef_System_Type_">CreateObjRef</a></span></span></td>
<td><span data-ttu-id="81210-165">(Se hereda de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-165">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="81210-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span><span class="sxs-lookup"><span data-stu-id="81210-167"><a href="/dotnet/api/system.io.stream.createwaithandle#System_IO_Stream_CreateWaitHandle">CreateWaitHandle</a></span></span></td>
<td><span data-ttu-id="81210-168"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="81210-168"><strong>Obsolete.</strong></span></span> <span data-ttu-id="81210-169">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-169">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="81210-171"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="81210-172">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-172">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="81210-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="81210-174"><a href="/dotnet/api/system.io.stream.dispose#System_IO_Stream_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="81210-175">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-175">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span><span class="sxs-lookup"><span data-stu-id="81210-177"><a href="/dotnet/api/system.io.stream.endread#System_IO_Stream_EndRead_System_IAsyncResult_">EndRead</a></span></span></td>
<td><span data-ttu-id="81210-178">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-178">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span><span class="sxs-lookup"><span data-stu-id="81210-180"><a href="/dotnet/api/system.io.stream.endwrite#System_IO_Stream_EndWrite_System_IAsyncResult_">EndWrite</a></span></span></td>
<td><span data-ttu-id="81210-181">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-181">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></span><span class="sxs-lookup"><span data-stu-id="81210-183"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="81210-184">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-184">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="81210-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="81210-186"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="81210-187">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-187">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-189"><a href="dn334193(v=exchg.10).md">Vaciar</a></span><span class="sxs-lookup"><span data-stu-id="81210-189"><a href="dn334193(v=exchg.10).md">Flush</a></span></span></td>
<td><span data-ttu-id="81210-190">Vacíe el flujo.</span><span class="sxs-lookup"><span data-stu-id="81210-190">Flush the stream.</span></span> <span data-ttu-id="81210-191">(Invalida <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream. Flush ()</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-191">(Overrides <a href="/dotnet/api/system.io.stream.flush#System_IO_Stream_Flush">Stream.Flush()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="81210-193"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="81210-194">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-194">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="81210-196"><a href="/dotnet/api/system.marshalbyrefobject.getlifetimeservice#System_MarshalByRefObject_GetLifetimeService">GetLifetimeService</a></span></span></td>
<td><span data-ttu-id="81210-197">(Se hereda de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-197">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="81210-199"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="81210-200">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-200">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span><span class="sxs-lookup"><span data-stu-id="81210-202"><a href="/dotnet/api/system.marshalbyrefobject.initializelifetimeservice#System_MarshalByRefObject_InitializeLifetimeService">InitializeLifetimeService</a></span></span></td>
<td><span data-ttu-id="81210-203">(Se hereda de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-203">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="81210-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone ()</a></span><span class="sxs-lookup"><span data-stu-id="81210-205"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone()</a></span></span></td>
<td><span data-ttu-id="81210-206">(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-206">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><span data-ttu-id="81210-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone (booleano)</a></span><span class="sxs-lookup"><span data-stu-id="81210-208"><a href="/dotnet/api/system.marshalbyrefobject.memberwiseclone#System_MarshalByRefObject_MemberwiseClone_System_Boolean_">MemberwiseClone(Boolean)</a></span></span></td>
<td><span data-ttu-id="81210-209">(Se hereda de <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-209">(Inherited from <a href="/dotnet/api/system.marshalbyrefobject">MarshalByRefObject</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-211"><a href="dn334198(v=exchg.10).md">Lectura</a></span><span class="sxs-lookup"><span data-stu-id="81210-211"><a href="dn334198(v=exchg.10).md">Read</a></span></span></td>
<td><span data-ttu-id="81210-212">Lee una secuencia de bytes en el flujo actual y avanza la posición en el flujo según el número de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="81210-212">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span> <span data-ttu-id="81210-213">(Invalida <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream. Read ([], Int32, Int32)</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-213">(Overrides <a href="/dotnet/api/system.io.stream.read#System_IO_Stream_Read_System_Byte___System_Int32_System_Int32_">Stream.Read([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span><span class="sxs-lookup"><span data-stu-id="81210-215"><a href="/dotnet/api/system.io.stream.readbyte#System_IO_Stream_ReadByte">ReadByte</a></span></span></td>
<td><span data-ttu-id="81210-216">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-216">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-218"><a href="dn334154(v=exchg.10).md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="81210-218"><a href="dn334154(v=exchg.10).md">Seek</a></span></span></td>
<td><span data-ttu-id="81210-219">Establece la posición en la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="81210-219">Sets the position in the current stream.</span></span> <span data-ttu-id="81210-220">(Invalida <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream. Seek (Int64, SeekOrigin)</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-220">(Overrides <a href="/dotnet/api/system.io.stream.seek#System_IO_Stream_Seek_System_Int64_System_IO_SeekOrigin_">Stream.Seek(Int64, SeekOrigin)</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span><span class="sxs-lookup"><span data-stu-id="81210-222"><a href="dn334196(v=exchg.10).md">SetLength</a></span></span></td>
<td><span data-ttu-id="81210-223">Establece la longitud del flujo.</span><span class="sxs-lookup"><span data-stu-id="81210-223">Sets the length of the stream.</span></span> <span data-ttu-id="81210-224">(Invalida <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream. SetLength (Int64)</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-224">(Overrides <a href="/dotnet/api/system.io.stream.setlength#System_IO_Stream_SetLength_System_Int64_">Stream.SetLength(Int64)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-226"><a href="dn334149(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="81210-226"><a href="dn334149(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="81210-227">Devuelve una <a href="/dotnet/api/system.string">cadena</a> que representa el <a href="dn334143(v=exchg.10).md">ColumnStream</a>actual.</span><span class="sxs-lookup"><span data-stu-id="81210-227">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn334143(v=exchg.10).md">ColumnStream</a>.</span></span> <span data-ttu-id="81210-228">(Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-228">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-230"><a href="dn334197(v=exchg.10).md">Escritura</a></span><span class="sxs-lookup"><span data-stu-id="81210-230"><a href="dn334197(v=exchg.10).md">Write</a></span></span></td>
<td><span data-ttu-id="81210-231">Escribe una secuencia de bytes en la secuencia actual y avanza la posición actual en esta secuencia según el número de bytes escritos.</span><span class="sxs-lookup"><span data-stu-id="81210-231">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span> <span data-ttu-id="81210-232">(Invalida <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream. Write ([], Int32, Int32)</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-232">(Overrides <a href="/dotnet/api/system.io.stream.write#System_IO_Stream_Write_System_Byte___System_Int32_System_Int32_">Stream.Write([], Int32, Int32)</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><span data-ttu-id="81210-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span><span class="sxs-lookup"><span data-stu-id="81210-234"><a href="/dotnet/api/system.io.stream.writebyte#System_IO_Stream_WriteByte_System_Byte_">WriteByte</a></span></span></td>
<td><span data-ttu-id="81210-235">(Se hereda de <a href="/dotnet/api/system.io.stream">Stream</a>).</span><span class="sxs-lookup"><span data-stu-id="81210-235">(Inherited from <a href="/dotnet/api/system.io.stream">Stream</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="81210-236">Superior</span><span class="sxs-lookup"><span data-stu-id="81210-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="81210-237">Vea también</span><span class="sxs-lookup"><span data-stu-id="81210-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="81210-238">Referencia</span><span class="sxs-lookup"><span data-stu-id="81210-238">Reference</span></span>

[<span data-ttu-id="81210-239">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="81210-239">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="81210-240">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="81210-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
