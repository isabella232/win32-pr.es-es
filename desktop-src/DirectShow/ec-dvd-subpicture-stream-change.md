---
description: Indica que el número de secuencia de subimagen actual ha cambiado para el título principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 21549ec6427b82c6d229d2e3962689bc8879815429f3a68fd32d54283c30d6a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639775"
---
# <a name="ec_dvd_subpicture_stream_change"></a>CAMBIO \_ DE SECUENCIA DE \_ SUBASPECCIÓN \_ DE DVD DE \_ EC

Indica que el número de secuencia de subimagen actual ha cambiado para el título principal.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica el nuevo número de secuencia de subaspección de usuario. Los números de secuencia de subaspección van de 0 a 31. Stream 0xFFFFFFFF indica que no se ha seleccionado ninguna secuencia.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor booleano que indica el estado de encendido y apagado de la subaspección.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La subaspección puede cambiar automáticamente con un comando de navegación que se crea en el disco, así como a través del control de aplicación [**mediante IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).

Este evento se genera en todos los dominios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




