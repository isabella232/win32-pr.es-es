---
description: 'Más información sobre: SystemParameters.Configpropiedad primario'
title: SystemParameters.Configpropiedad primario
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910221"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="33e53-103">SystemParameters.Configpropiedad primario</span><span class="sxs-lookup"><span data-stu-id="33e53-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="33e53-104">Obtiene o establece un valor que especifica los valores predeterminados para todo el conjunto de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="33e53-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="33e53-105">Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración.</span><span class="sxs-lookup"><span data-stu-id="33e53-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="33e53-106">Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="33e53-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="33e53-107">Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="33e53-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="33e53-108">Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</span><span class="sxs-lookup"><span data-stu-id="33e53-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="33e53-109">Compatible con Windows Vista y up.</span><span class="sxs-lookup"><span data-stu-id="33e53-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="33e53-110">Se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="33e53-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="33e53-111">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33e53-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33e53-112">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33e53-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33e53-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33e53-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="33e53-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="33e53-114">Property value</span></span>

<span data-ttu-id="33e53-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="33e53-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="33e53-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="33e53-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33e53-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="33e53-117">Reference</span></span>

[<span data-ttu-id="33e53-118">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="33e53-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="33e53-119">Miembros de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="33e53-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="33e53-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="33e53-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
