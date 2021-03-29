---
description: 'Más información sobre: VistaGrbits. IndexCrossProduct, campo'
title: Campo VistaGrbits. IndexCrossProduct (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003167"
---
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="9919f-103">VistaGrbits. IndexCrossProduct, campo</span><span class="sxs-lookup"><span data-stu-id="9919f-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="9919f-104">Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna con varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave.</span><span class="sxs-lookup"><span data-stu-id="9919f-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="9919f-105">De lo contrario, el índice solo tendrá una entrada para cada valor múltiple de la columna de clave más importante que sea una columna con varios valores y cada una de esas entradas de índice usaría el primer valor entre las demás columnas de clave que son columnas con varios valores.</span><span class="sxs-lookup"><span data-stu-id="9919f-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="9919f-106">Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores "rojo" y "azul" y sobre la columna B que tiene los valores "1" y "2", se crearán las siguientes entradas de índice: "rojo", "1"; "rojo", "2"; "Blue", "1"; "Blue", "2".</span><span class="sxs-lookup"><span data-stu-id="9919f-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="9919f-107">De lo contrario, se crearán las siguientes entradas de índice: "red", "1"; "Blue", "1".</span><span class="sxs-lookup"><span data-stu-id="9919f-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="9919f-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9919f-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9919f-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9919f-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9919f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9919f-110">Syntax</span></span>

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a><span data-ttu-id="9919f-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9919f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9919f-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="9919f-112">Reference</span></span>

[<span data-ttu-id="9919f-113">Clase VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="9919f-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="9919f-114">Miembros de VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="9919f-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="9919f-115">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="9919f-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
