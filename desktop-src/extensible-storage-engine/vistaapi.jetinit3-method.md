---
description: 'Más información sobre: VistaApi. JetInit3 (método)'
title: Método VistaApi. JetInit3 (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705743"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="2a12c-103">VistaApi. JetInit3, método</span><span class="sxs-lookup"><span data-stu-id="2a12c-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="2a12c-104">Inicialice el motor de base de datos ESENT.</span><span class="sxs-lookup"><span data-stu-id="2a12c-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="2a12c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2a12c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2a12c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2a12c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2a12c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a12c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="2a12c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a12c-108">Parameters</span></span>

  - <span data-ttu-id="2a12c-109">instance</span><span class="sxs-lookup"><span data-stu-id="2a12c-109">instance</span></span>  
    <span data-ttu-id="2a12c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2a12c-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2a12c-111">Instancia de que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="2a12c-111">The instance to initialize.</span></span> <span data-ttu-id="2a12c-112">Si no se ha asignado una instancia, se crea una nueva y el motor funcionará en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="2a12c-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="2a12c-113">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="2a12c-113">recoveryOptions</span></span>  
    <span data-ttu-id="2a12c-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="2a12c-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="2a12c-115">Parámetros de recuperación adicionales para volver a asignar las bases de datos durante la recuperación, ubicación en la que detener la recuperación o en el estado de recuperación.</span><span class="sxs-lookup"><span data-stu-id="2a12c-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="2a12c-116">grbit</span><span class="sxs-lookup"><span data-stu-id="2a12c-116">grbit</span></span>  
    <span data-ttu-id="2a12c-117">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2a12c-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="2a12c-118">Opciones de inicialización.</span><span class="sxs-lookup"><span data-stu-id="2a12c-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2a12c-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a12c-119">Return value</span></span>

<span data-ttu-id="2a12c-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2a12c-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="2a12c-121">Código de advertencia.</span><span class="sxs-lookup"><span data-stu-id="2a12c-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2a12c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a12c-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2a12c-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="2a12c-123">Reference</span></span>

[<span data-ttu-id="2a12c-124">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="2a12c-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="2a12c-125">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="2a12c-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="2a12c-126">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="2a12c-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
