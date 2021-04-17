---
description: 'Más información sobre: SystemParameters. EnableAdvanced (propiedad)'
title: Propiedad SystemParameters. EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716819"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="30b80-103">Propiedad SystemParameters. EnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="30b80-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="30b80-104">Obtiene o establece un valor que indica si el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="30b80-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="30b80-105">Este parámetro se usa junto con la [configuración](./systemparameters.configuration-property.md) para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="30b80-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="30b80-106">Compatible con Windows Vista y up.</span><span class="sxs-lookup"><span data-stu-id="30b80-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="30b80-107">Se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="30b80-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="30b80-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30b80-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30b80-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="30b80-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30b80-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30b80-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="30b80-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="30b80-111">Property value</span></span>

<span data-ttu-id="30b80-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="30b80-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="30b80-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="30b80-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30b80-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="30b80-114">Reference</span></span>

[<span data-ttu-id="30b80-115">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="30b80-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="30b80-116">Miembros de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="30b80-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="30b80-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="30b80-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
