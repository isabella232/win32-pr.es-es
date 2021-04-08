---
description: 'Más información sobre: VistaApi. JetGetInstanceMiscInfo (método)'
title: Método VistaApi. JetGetInstanceMiscInfo (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908512"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="ed9f0-103">VistaApi. JetGetInstanceMiscInfo, método</span><span class="sxs-lookup"><span data-stu-id="ed9f0-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="ed9f0-104">Recupera información sobre una instancia de.</span><span class="sxs-lookup"><span data-stu-id="ed9f0-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="ed9f0-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed9f0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ed9f0-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed9f0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9f0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed9f0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="ed9f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed9f0-108">Parameters</span></span>

  - <span data-ttu-id="ed9f0-109">instance</span><span class="sxs-lookup"><span data-stu-id="ed9f0-109">instance</span></span>  
    <span data-ttu-id="ed9f0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed9f0-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="ed9f0-111">Instancia de en la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="ed9f0-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed9f0-112">firma</span><span class="sxs-lookup"><span data-stu-id="ed9f0-112">signature</span></span>  
    <span data-ttu-id="ed9f0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ed9f0-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="ed9f0-114">Información recuperada.</span><span class="sxs-lookup"><span data-stu-id="ed9f0-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed9f0-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="ed9f0-115">infoLevel</span></span>  
    <span data-ttu-id="ed9f0-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ed9f0-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="ed9f0-117">Tipo de información que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ed9f0-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed9f0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed9f0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed9f0-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="ed9f0-119">Reference</span></span>

[<span data-ttu-id="ed9f0-120">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="ed9f0-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="ed9f0-121">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="ed9f0-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="ed9f0-122">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="ed9f0-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
