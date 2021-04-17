---
description: 'Más información acerca de: propiedad JET_INSTANCE_INFO. szDatabaseFileName'
title: Propiedad JET_INSTANCE_INFO. szDatabaseFileName
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688524"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a><span data-ttu-id="97eb6-103">Propiedad JET_INSTANCE_INFO. szDatabaseFileName</span><span class="sxs-lookup"><span data-stu-id="97eb6-103">JET_INSTANCE_INFO.szDatabaseFileName property</span></span>

<span data-ttu-id="97eb6-104">Obtiene una colección de cadenas, cada una de las cuales contiene el nombre de archivo de una base de datos que se adjunta a la instancia de base de datos.</span><span class="sxs-lookup"><span data-stu-id="97eb6-104">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="97eb6-105">La matriz tiene elementos cDatabases.</span><span class="sxs-lookup"><span data-stu-id="97eb6-105">The array has cDatabases elements.</span></span>

<span data-ttu-id="97eb6-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97eb6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97eb6-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97eb6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97eb6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97eb6-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a><span data-ttu-id="97eb6-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="97eb6-109">Property value</span></span>

<span data-ttu-id="97eb6-110">Tipo: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="97eb6-110">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="97eb6-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="97eb6-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97eb6-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="97eb6-112">Reference</span></span>

[<span data-ttu-id="97eb6-113">JET_INSTANCE_INFO (clase)</span><span class="sxs-lookup"><span data-stu-id="97eb6-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="97eb6-114">Miembros de JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="97eb6-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="97eb6-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="97eb6-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
