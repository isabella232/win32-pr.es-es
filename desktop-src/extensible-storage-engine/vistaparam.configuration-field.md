---
description: 'Más información acerca de: VistaParam.Configcampo primario'
title: VistaParam.Configcampo primario (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808420"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="474b9-103">VistaParam.Configcampo primario</span><span class="sxs-lookup"><span data-stu-id="474b9-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="474b9-104">Este parámetro expone varios conjuntos de valores predeterminados para todo el conjunto de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="474b9-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="474b9-105">Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración.</span><span class="sxs-lookup"><span data-stu-id="474b9-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="474b9-106">Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="474b9-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="474b9-107">Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="474b9-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="474b9-108">Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</span><span class="sxs-lookup"><span data-stu-id="474b9-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="474b9-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="474b9-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="474b9-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="474b9-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="474b9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="474b9-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="474b9-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="474b9-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="474b9-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="474b9-113">Reference</span></span>

[<span data-ttu-id="474b9-114">Clase VistaParam</span><span class="sxs-lookup"><span data-stu-id="474b9-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="474b9-115">Miembros de VistaParam</span><span class="sxs-lookup"><span data-stu-id="474b9-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="474b9-116">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="474b9-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
