---
description: 'Más información acerca de: estructura de JET_INDEXID'
title: Estructura de JET_INDEXID
TOCTitle: JET_INDEXID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_INDEXID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid(v=EXCHG.10)
ms:contentKeyID: 39510071
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13ff0984926fe821d666d18c1907c9bd1bf93b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716975"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="4dbd6-103">Estructura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4dbd6-103">JET_INDEXID structure</span></span>

<span data-ttu-id="4dbd6-104">Contiene un identificador de índice.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-104">Holds an index ID.</span></span> <span data-ttu-id="4dbd6-105">Un ID. de índice es una sugerencia que se usa para acelerar la selección del índice actual mediante JetSetCurrentIndex.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-105">An index ID is a hint that is used to accelerate the selection of the current index using JetSetCurrentIndex.</span></span> <span data-ttu-id="4dbd6-106">Resulta muy útil cuando hay un gran número de índices en una tabla.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-106">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="4dbd6-107">El identificador de índice se puede recuperar mediante JetGetIndexInfo o JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-107">The index ID can be retrieved using JetGetIndexInfo or JetGetTableIndexInfo.</span></span>

<span data-ttu-id="4dbd6-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4dbd6-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4dbd6-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4dbd6-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4dbd6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4dbd6-110">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_INDEXID _
    Implements IEquatable(Of JET_INDEXID)
'Usage
Dim instance As JET_INDEXID
```

``` csharp
public struct JET_INDEXID : IEquatable<JET_INDEXID>
```

## <a name="remarks"></a><span data-ttu-id="4dbd6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4dbd6-111">Remarks</span></span>

<span data-ttu-id="4dbd6-112">El atributo Pack es necesario porque la versión de C++ se define como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-112">The Pack attribute is necessary because the C++ version is defined as a byte array.</span></span> <span data-ttu-id="4dbd6-113">Si el \# compilador de C inserta el relleno habitual entre el uint cbStruct y el IntPtr, la estructura acaba demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-113">If the C\# compiler inserts the usual padding between the uint cbStruct and the IntPtr, then the structure ends up too large.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="4dbd6-114">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="4dbd6-114">Thread safety</span></span>

<span data-ttu-id="4dbd6-115">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4dbd6-116">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4dbd6-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="4dbd6-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4dbd6-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="4dbd6-118">Reference</span></span>

[<span data-ttu-id="4dbd6-119">Miembros de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="4dbd6-119">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="4dbd6-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4dbd6-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
