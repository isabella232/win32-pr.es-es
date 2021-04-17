---
description: 'Más información sobre: InstanceParameters. MaxTemporaryTables (propiedad)'
title: Propiedad InstanceParameters. MaxTemporaryTables
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716547"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="2b632-103">Propiedad InstanceParameters. MaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="2b632-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="2b632-104">Obtiene o establece el número de recursos de tabla temporal que va a usar una instancia de.</span><span class="sxs-lookup"><span data-stu-id="2b632-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="2b632-105">Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="2b632-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="2b632-106">Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="2b632-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="2b632-107">Esta configuración puede ser útil para evitar la e/s necesaria para crear la base de datos temporal si se sabe que no se va a usar.</span><span class="sxs-lookup"><span data-stu-id="2b632-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="2b632-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b632-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2b632-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2b632-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b632-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b632-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2b632-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2b632-111">Property value</span></span>

<span data-ttu-id="2b632-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2b632-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="2b632-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b632-113">Remarks</span></span>

<span data-ttu-id="2b632-114">El uso de una tabla temporal también requiere un recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="2b632-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b632-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b632-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b632-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="2b632-116">Reference</span></span>

[<span data-ttu-id="2b632-117">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="2b632-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="2b632-118">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="2b632-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="2b632-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2b632-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
