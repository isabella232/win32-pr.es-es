---
title: Enumeración WMT_RIGHTS (wmdrmsdk. h)
description: Define los derechos que se pueden especificar en una licencia de DRM.
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 644cff9c94876fab11bc9fbe181ac0375d9444fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708141"
---
# <a name="wmt_rights-enumeration"></a><span data-ttu-id="ba04f-105">\_Enumeración de derechos WMT</span><span class="sxs-lookup"><span data-stu-id="ba04f-105">WMT\_RIGHTS enumeration</span></span>

<span data-ttu-id="ba04f-106">El tipo de enumeración de **\_ derechos WMT** define los derechos que se pueden especificar en una licencia de DRM.</span><span class="sxs-lookup"><span data-stu-id="ba04f-106">The **WMT\_RIGHTS** enumeration type defines the rights that may be specified in a DRM license.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba04f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba04f-107">Syntax</span></span>


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a><span data-ttu-id="ba04f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="ba04f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ba04f-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**\_reproducción correcta de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-109"><span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT\_RIGHT\_PLAYBACK**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-110">Especifica el derecho para reproducir contenido sin restricciones.</span><span class="sxs-lookup"><span data-stu-id="ba04f-110">Specifies the right to play content without restriction.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**\_copia derecha \_ \_ de WMT en un \_ dispositivo que no es de \_ SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-111"><span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-112">Especifica el derecho para copiar contenido en un dispositivo no compatible con la iniciativa de música digital segura (SDMI).</span><span class="sxs-lookup"><span data-stu-id="ba04f-112">Specifies the right to copy content to a device not compliant with the Secure Digital Music Initiative (SDMI).</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**\_copia correcta del WMT \_ \_ en el \_ CD**</span><span class="sxs-lookup"><span data-stu-id="ba04f-113"><span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT\_RIGHT\_COPY\_TO\_CD**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-114">Especifica el derecho para copiar contenido en un CD.</span><span class="sxs-lookup"><span data-stu-id="ba04f-114">Specifies the right to copy content to a CD.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**\_copia correcta \_ \_ de WMT en el \_ dispositivo de SDMI \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-115"><span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-116">Especifica el derecho para copiar contenido en un dispositivo compatible con SDMI.</span><span class="sxs-lookup"><span data-stu-id="ba04f-116">Specifies the right to copy content to a device compliant with the SDMI.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ justo \_ una \_ vez**</span><span class="sxs-lookup"><span data-stu-id="ba04f-117"><span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT\_RIGHT\_ONE\_TIME**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-118">Especifica el derecho para reproducir contenido solo una vez.</span><span class="sxs-lookup"><span data-stu-id="ba04f-118">Specifies the right to play content one time only.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**la \_ secuencia de guardado del derecho WMT está \_ \_ \_ protegida**</span><span class="sxs-lookup"><span data-stu-id="ba04f-119"><span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT\_RIGHT\_SAVE\_STREAM\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-120">Especifica el derecho para guardar el contenido de un servidor.</span><span class="sxs-lookup"><span data-stu-id="ba04f-120">Specifies the right to save content from a server.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**\_copia correcta de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-121"><span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT\_RIGHT\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-122">Especifica el derecho para copiar contenido.</span><span class="sxs-lookup"><span data-stu-id="ba04f-122">Specifies the right to copy content.</span></span> <span data-ttu-id="ba04f-123">Windows Media DRM 10 regula los dispositivos en los que se puede copiar el contenido mediante el uso de los niveles de protección de salida (OPLs).</span><span class="sxs-lookup"><span data-stu-id="ba04f-123">Windows Media DRM 10 regulates the devices to which the content can be copied by using output protection levels (OPLs).</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**\_ \_ reproducción colaborativa correcta de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-124"><span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT\_RIGHT\_COLLABORATIVE\_PLAY**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-125">Especifica el derecho para reproducir contenido como parte de un escenario en línea en el que varios participantes pueden aportar canciones de su colección a una lista de reproducción compartida.</span><span class="sxs-lookup"><span data-stu-id="ba04f-125">Specifies the right to play content as part of an online scenario where multiple participants can contribute songs from their collection to a shared playlist.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**\_ \_ desencadenador de SDMI de la derecha WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba04f-126"><span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT\_RIGHT\_SDMI\_TRIGGER**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ba04f-127">Reserved for future use.</span></span> <span data-ttu-id="ba04f-128">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ba04f-128">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ba04f-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ right \_ SDMI \_ NOMORECOPIES**</span><span class="sxs-lookup"><span data-stu-id="ba04f-129"><span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT\_RIGHT\_SDMI\_NOMORECOPIES**</span></span>
</dt> <dd>

<span data-ttu-id="ba04f-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ba04f-130">Reserved for future use.</span></span> <span data-ttu-id="ba04f-131">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="ba04f-131">Do not use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba04f-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba04f-132">Remarks</span></span>

<span data-ttu-id="ba04f-133">Estos valores son marcas de bits, por lo que se pueden establecer uno o varios combinando con **el operador OR** bit a bit.</span><span class="sxs-lookup"><span data-stu-id="ba04f-133">These values are bit flags, so one or more can be set by combining them with the bitwise **OR** operator.</span></span>

<span data-ttu-id="ba04f-134">Al usar Windows Media DRM 10, **la \_ \_ copia correcta \_ de WMT en un \_ \_ \_ dispositivo que no es de SDMI**, la **\_ \_ copia correcta de WMT en el \_ \_ \_ dispositivo de SDMI** y la **\_ \_ copia correcta de WMT en el \_ \_ CD** se sustituyen por la **\_ \_ copia correcta de WMT**.</span><span class="sxs-lookup"><span data-stu-id="ba04f-134">When using Windows Media DRM 10, **WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE**, **WMT\_RIGHT\_COPY\_TO\_SDMI\_DEVICE**, and **WMT\_RIGHT\_COPY\_TO\_CD** are superseded by **WMT\_RIGHT\_COPY**.</span></span> <span data-ttu-id="ba04f-135">Las limitaciones de los dispositivos en los que se puede copiar el contenido se especifican mediante los niveles de protección de la salida (OPLs).</span><span class="sxs-lookup"><span data-stu-id="ba04f-135">Limitations on the devices to which the content may be copied are specified by using output protection levels (OPLs).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba04f-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba04f-136">Requirements</span></span>



| <span data-ttu-id="ba04f-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba04f-137">Requirement</span></span> | <span data-ttu-id="ba04f-138">Value</span><span class="sxs-lookup"><span data-stu-id="ba04f-138">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba04f-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba04f-139">Header</span></span><br/> | <dl> <span data-ttu-id="ba04f-140"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba04f-140"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba04f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba04f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba04f-142">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="ba04f-142">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





