---
description: 'Más información sobre: SystemParameters. OutstandingIOMax (propiedad)'
title: Propiedad SystemParameters. OutstandingIOMax
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545739"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="19b7a-103">Propiedad SystemParameters. OutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="19b7a-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="19b7a-104">Este parámetro controla el número de operaciones de e/s de archivos de base de datos que se pueden poner en cola por disco en el sistema operativo host al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="19b7a-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="19b7a-105">Un valor mayor para este parámetro puede ayudar significativamente al rendimiento de una aplicación de base de datos grande.</span><span class="sxs-lookup"><span data-stu-id="19b7a-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="19b7a-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19b7a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19b7a-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19b7a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19b7a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19b7a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="19b7a-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="19b7a-109">Property value</span></span>

<span data-ttu-id="19b7a-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="19b7a-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="19b7a-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="19b7a-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19b7a-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="19b7a-112">Reference</span></span>

[<span data-ttu-id="19b7a-113">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="19b7a-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="19b7a-114">Miembros de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="19b7a-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="19b7a-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="19b7a-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
