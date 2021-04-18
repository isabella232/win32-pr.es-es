---
title: Enumeración RemoteSessionActionType
description: Se utiliza para especificar el tipo de acción remota.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto enumeración RemoteSessionActionType
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685922"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="650f2-104">Enumeración RemoteSessionActionType</span><span class="sxs-lookup"><span data-stu-id="650f2-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="650f2-105">Se utiliza para especificar el tipo de acción remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="650f2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="650f2-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="650f2-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="650f2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="650f2-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span><span class="sxs-lookup"><span data-stu-id="650f2-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-109">Muestra los accesos en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="650f2-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span><span class="sxs-lookup"><span data-stu-id="650f2-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-111">Muestra la barra de la aplicación en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="650f2-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span><span class="sxs-lookup"><span data-stu-id="650f2-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-113">Acopla la aplicación en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-113">Docks the application in the remote session.</span></span> <span data-ttu-id="650f2-114">Esta opción está en desuso y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="650f2-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="650f2-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span><span class="sxs-lookup"><span data-stu-id="650f2-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-116">Hace que la pantalla Inicio se muestre en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="650f2-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span><span class="sxs-lookup"><span data-stu-id="650f2-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-118">Hace que la ventana de conmutador de la aplicación se muestre en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="650f2-119">Es el mismo que el usuario que presiona Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="650f2-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="650f2-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span><span class="sxs-lookup"><span data-stu-id="650f2-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="650f2-121">Hace que el centro de actividades se muestre en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="650f2-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="650f2-122">Esto es lo mismo que el usuario que presiona Win + A.</span><span class="sxs-lookup"><span data-stu-id="650f2-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="650f2-123">**Windows server 2012 R2, Windows 8.1, Windows server 2012 y Windows 8:** Este valor no se admite antes de Windows Server 2016 y Windows 10.</span><span class="sxs-lookup"><span data-stu-id="650f2-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="650f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="650f2-124">Requirements</span></span>



| <span data-ttu-id="650f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="650f2-125">Requirement</span></span> | <span data-ttu-id="650f2-126">Value</span><span class="sxs-lookup"><span data-stu-id="650f2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="650f2-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="650f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="650f2-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="650f2-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="650f2-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="650f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="650f2-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="650f2-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="650f2-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="650f2-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="650f2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="650f2-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="650f2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="650f2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="650f2-134">**IMsRdpClient8::SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="650f2-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





