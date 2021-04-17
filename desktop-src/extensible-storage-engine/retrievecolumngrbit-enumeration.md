---
description: 'Más información sobre: enumeración RetrieveColumnGrbit'
title: Enumeración RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a223a288b8ad2d2e976be3bb9f2f524f78b9a8fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687675"
---
# <a name="retrievecolumngrbit-enumeration"></a><span data-ttu-id="0c48f-103">Enumeración RetrieveColumnGrbit</span><span class="sxs-lookup"><span data-stu-id="0c48f-103">RetrieveColumnGrbit enumeration</span></span>

<span data-ttu-id="0c48f-104">Opciones de JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="0c48f-104">Options for JetRetrieveColumn.</span></span>

<span data-ttu-id="0c48f-105">Esta enumeración tiene un atributo [FlagsAttribute](/dotnet/api/system.flagsattribute), que permite una combinación bit a bit de sus valores de miembro.</span><span class="sxs-lookup"><span data-stu-id="0c48f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0c48f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c48f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c48f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c48f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c48f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c48f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a><span data-ttu-id="0c48f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c48f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0c48f-110">Nombre del miembro</span><span class="sxs-lookup"><span data-stu-id="0c48f-110">Member name</span></span></th>
<th><span data-ttu-id="0c48f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c48f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c48f-112">None</span><span class="sxs-lookup"><span data-stu-id="0c48f-112">None</span></span></td>
<td><span data-ttu-id="0c48f-113">Opciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="0c48f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c48f-114">RetrieveCopy</span><span class="sxs-lookup"><span data-stu-id="0c48f-114">RetrieveCopy</span></span></td>
<td><span data-ttu-id="0c48f-115">Esta marca hace que la columna de recuperación recupere el valor modificado en lugar del valor original.</span><span class="sxs-lookup"><span data-stu-id="0c48f-115">This flag causes retrieve column to retrieve the modified value instead of the original value.</span></span> <span data-ttu-id="0c48f-116">Si el valor no se ha modificado, se recupera el valor original.</span><span class="sxs-lookup"><span data-stu-id="0c48f-116">If the value has not been modified, then the original value is retrieved.</span></span> <span data-ttu-id="0c48f-117">De esta manera, se puede recuperar un valor que todavía no se ha insertado o actualizado durante la operación de inserción o actualización de un registro.</span><span class="sxs-lookup"><span data-stu-id="0c48f-117">In this way, a value that has not yet been inserted or updated may be retrieved during the operation of inserting or updating a record.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c48f-118">RetrieveFromIndex</span><span class="sxs-lookup"><span data-stu-id="0c48f-118">RetrieveFromIndex</span></span></td>
<td><span data-ttu-id="0c48f-119">Esta opción se utiliza para recuperar los valores de columna del índice, si es posible, sin tener acceso al registro.</span><span class="sxs-lookup"><span data-stu-id="0c48f-119">This option is used to retrieve column values from the index, if possible, without accessing the record.</span></span> <span data-ttu-id="0c48f-120">De esta manera, se puede evitar la carga innecesaria de registros cuando los datos necesarios están disponibles en las propias entradas de índice.</span><span class="sxs-lookup"><span data-stu-id="0c48f-120">In this way, unnecessary loading of records can be avoided when needed data is available from index entries themselves.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c48f-121">RetrieveFromPrimaryBookmark</span><span class="sxs-lookup"><span data-stu-id="0c48f-121">RetrieveFromPrimaryBookmark</span></span></td>
<td><span data-ttu-id="0c48f-122">Esta opción se usa para recuperar valores de columna del marcador de índice y puede diferir del valor de índice cuando una columna aparece en el índice principal y en el índice actual.</span><span class="sxs-lookup"><span data-stu-id="0c48f-122">This option is used to retrieve column values from the index bookmark, and may differ from the index value when a column appears both in the primary index and the current index.</span></span> <span data-ttu-id="0c48f-123">Esta opción no se debe especificar si el índice actual es el índice clúster o principal.</span><span class="sxs-lookup"><span data-stu-id="0c48f-123">This option should not be specified if the current index is the clustered, or primary, index.</span></span> <span data-ttu-id="0c48f-124">No se puede establecer este bit si también se establece RetrieveFromIndex.</span><span class="sxs-lookup"><span data-stu-id="0c48f-124">This bit cannot be set if RetrieveFromIndex is also set.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c48f-125">RetrieveTag</span><span class="sxs-lookup"><span data-stu-id="0c48f-125">RetrieveTag</span></span></td>
<td><span data-ttu-id="0c48f-126">Esta opción se usa para recuperar el número de secuencia de un valor de columna de varios valores en JET_RETINFO. itagSequence.</span><span class="sxs-lookup"><span data-stu-id="0c48f-126">This option is used to retrieve the sequence number of a multi-valued column value in JET_RETINFO.itagSequence.</span></span> <span data-ttu-id="0c48f-127">Recuperar el número de secuencia puede ser una operación costosa y solo debe realizarse si es necesario.</span><span class="sxs-lookup"><span data-stu-id="0c48f-127">Retrieving the sequence number can be a costly operation and should only be done if necessary.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0c48f-128">RetrieveNull</span><span class="sxs-lookup"><span data-stu-id="0c48f-128">RetrieveNull</span></span></td>
<td><span data-ttu-id="0c48f-129">Esta opción se usa para recuperar los valores NULL de las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="0c48f-129">This option is used to retrieve multi-valued column NULL values.</span></span> <span data-ttu-id="0c48f-130">Si no se especifica esta opción, se omitirán automáticamente los valores NULL de las columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="0c48f-130">If this option is not specified, multi-valued column NULL values will automatically be skipped.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0c48f-131">RetrieveIgnoreDefault</span><span class="sxs-lookup"><span data-stu-id="0c48f-131">RetrieveIgnoreDefault</span></span></td>
<td><span data-ttu-id="0c48f-132">Esta opción solo afecta a las columnas con varios valores y hace que se devuelva un valor NULL cuando el número de secuencia solicitado es 1 y no hay valores establecidos para la columna en el registro.</span><span class="sxs-lookup"><span data-stu-id="0c48f-132">This option affects only multi-valued columns and causes a NULL value to be returned when the requested sequence number is 1 and there are no set values for the column in the record.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0c48f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c48f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c48f-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="0c48f-134">Reference</span></span>

[<span data-ttu-id="0c48f-135">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0c48f-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
