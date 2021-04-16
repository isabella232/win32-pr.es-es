---
description: 'Más información acerca de: método Instance.Init (JET_RSTINFO, InitGrbit)'
title: Método Instance.Init (JET_RSTINFO, InitGrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705821"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="3c1b2-103">Método Instance.Init (JET_RSTINFO, InitGrbit)</span><span class="sxs-lookup"><span data-stu-id="3c1b2-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="3c1b2-104">Inicialice el JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="3c1b2-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="3c1b2-105">Esta API requiere al menos la versión de vista de ESENT.</span><span class="sxs-lookup"><span data-stu-id="3c1b2-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="3c1b2-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3c1b2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3c1b2-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3c1b2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1b2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c1b2-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3c1b2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c1b2-109">Parameters</span></span>

  - <span data-ttu-id="3c1b2-110">recoveryOptions</span><span class="sxs-lookup"><span data-stu-id="3c1b2-110">recoveryOptions</span></span>  
    <span data-ttu-id="3c1b2-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="3c1b2-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="3c1b2-112">Parámetros de recuperación adicionales para volver a asignar las bases de datos durante la recuperación, ubicación en la que detener la recuperación o en el estado de recuperación.</span><span class="sxs-lookup"><span data-stu-id="3c1b2-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="3c1b2-113">grbit</span><span class="sxs-lookup"><span data-stu-id="3c1b2-113">grbit</span></span>  
    <span data-ttu-id="3c1b2-114">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3c1b2-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3c1b2-115">Opciones de inicialización.</span><span class="sxs-lookup"><span data-stu-id="3c1b2-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c1b2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c1b2-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3c1b2-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="3c1b2-117">Reference</span></span>

[<span data-ttu-id="3c1b2-118">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="3c1b2-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="3c1b2-119">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="3c1b2-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="3c1b2-120">Sobrecarga init</span><span class="sxs-lookup"><span data-stu-id="3c1b2-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="3c1b2-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3c1b2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
