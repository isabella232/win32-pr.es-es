---
description: 'Más información acerca de: estructura de JET_DBID'
title: Estructura de JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910490"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="521d8-103">Estructura de JET_DBID</span><span class="sxs-lookup"><span data-stu-id="521d8-103">JET_DBID structure</span></span>

<span data-ttu-id="521d8-104">Un JET_DBID contiene el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="521d8-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="521d8-105">Un identificador de base de datos se utiliza para administrar el esquema de una base de datos.</span><span class="sxs-lookup"><span data-stu-id="521d8-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="521d8-106">También se puede usar para administrar las tablas dentro de esa base de datos.</span><span class="sxs-lookup"><span data-stu-id="521d8-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="521d8-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="521d8-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="521d8-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="521d8-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="521d8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="521d8-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="521d8-110">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="521d8-110">Thread safety</span></span>

<span data-ttu-id="521d8-111">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="521d8-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="521d8-112">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="521d8-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="521d8-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="521d8-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="521d8-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="521d8-114">Reference</span></span>

[<span data-ttu-id="521d8-115">Miembros de JET_DBID</span><span class="sxs-lookup"><span data-stu-id="521d8-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="521d8-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="521d8-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
