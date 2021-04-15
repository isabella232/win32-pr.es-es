---
title: Evento Player. buffering
description: El evento de almacenamiento en búfer se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer. | Evento Player. buffering
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Almacenar en búfer ventanas de eventos Media Player
- Almacenar en búfer ventanas de eventos Media Player, clase Player
- Clase de reproductor Windows Media Player, evento de almacenamiento en búfer
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708764"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="52bb6-107">Evento Player. buffering</span><span class="sxs-lookup"><span data-stu-id="52bb6-107">Player.Buffering event</span></span>

<span data-ttu-id="52bb6-108">El evento de **almacenamiento en búfer** se produce cuando el control de Media Player de Windows comienza o finaliza la descarga o el almacenamiento en búfer.</span><span class="sxs-lookup"><span data-stu-id="52bb6-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="52bb6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52bb6-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="52bb6-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52bb6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52bb6-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="52bb6-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="52bb6-112">**Valor booleano** que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="52bb6-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="52bb6-113">Value</span><span class="sxs-lookup"><span data-stu-id="52bb6-113">Value</span></span> | <span data-ttu-id="52bb6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="52bb6-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="52bb6-115">true</span><span class="sxs-lookup"><span data-stu-id="52bb6-115">true</span></span>  | <span data-ttu-id="52bb6-116">El almacenamiento en búfer se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="52bb6-116">Buffering has started.</span></span> |
| <span data-ttu-id="52bb6-117">false</span><span class="sxs-lookup"><span data-stu-id="52bb6-117">false</span></span> | <span data-ttu-id="52bb6-118">El almacenamiento en búfer ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="52bb6-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52bb6-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52bb6-119">Return value</span></span>

<span data-ttu-id="52bb6-120">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="52bb6-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52bb6-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52bb6-121">Remarks</span></span>

<span data-ttu-id="52bb6-122">Utilice este evento para determinar cuándo se inicia o se detiene el almacenamiento en búfer o la descarga.</span><span class="sxs-lookup"><span data-stu-id="52bb6-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="52bb6-123">Puede usar el mismo bloque de eventos para ambos casos y probar la *red*. **bufferingProgress** y *red*. **downloadProgress** para determinar si Windows Media Player está almacenando en búfer o descargando contenido actualmente.</span><span class="sxs-lookup"><span data-stu-id="52bb6-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="52bb6-124">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="52bb6-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="52bb6-125">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="52bb6-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="52bb6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52bb6-126">Requirements</span></span>



| <span data-ttu-id="52bb6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="52bb6-127">Requirement</span></span> | <span data-ttu-id="52bb6-128">Value</span><span class="sxs-lookup"><span data-stu-id="52bb6-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52bb6-129">Versión</span><span class="sxs-lookup"><span data-stu-id="52bb6-129">Version</span></span><br/> | <span data-ttu-id="52bb6-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="52bb6-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="52bb6-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52bb6-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="52bb6-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52bb6-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52bb6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="52bb6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bb6-134">**Network. bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="52bb6-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="52bb6-135">**Network. downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="52bb6-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="52bb6-136">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="52bb6-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





