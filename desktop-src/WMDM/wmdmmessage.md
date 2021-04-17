---
title: Enumeración WMDMMessage
description: El tipo de enumeración WMDMMessage define los tipos y los Estados de los mensajes.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Enumeración WMDMMessage de Windows Media Administrador de dispositivos
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698690"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="f0fc5-104">Enumeración WMDMMessage</span><span class="sxs-lookup"><span data-stu-id="f0fc5-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="f0fc5-105">El tipo de enumeración **WMDMMessage** define los tipos y los Estados de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f0fc5-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0fc5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0fc5-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="f0fc5-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f0fc5-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f0fc5-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**\_llegada del \_ dispositivo de mensajes de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="f0fc5-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="f0fc5-109">Se ha conectado un dispositivo Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0fc5-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="f0fc5-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**\_eliminación de \_ dispositivos de mensajes de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="f0fc5-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="f0fc5-111">Se ha quitado un dispositivo Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0fc5-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="f0fc5-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**\_llegada del \_ medio de mensajes de WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="f0fc5-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="f0fc5-113">Los medios se han insertado en un dispositivo Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0fc5-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="f0fc5-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**eliminación de los medios de mensajes de WMDM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0fc5-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="f0fc5-115">Los medios se han quitado de un dispositivo Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f0fc5-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0fc5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0fc5-116">Requirements</span></span>



| <span data-ttu-id="f0fc5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0fc5-117">Requirement</span></span> | <span data-ttu-id="f0fc5-118">Value</span><span class="sxs-lookup"><span data-stu-id="f0fc5-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0fc5-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0fc5-119">Header</span></span><br/> | <dl> <span data-ttu-id="f0fc5-120"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0fc5-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0fc5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0fc5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0fc5-122">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="f0fc5-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





