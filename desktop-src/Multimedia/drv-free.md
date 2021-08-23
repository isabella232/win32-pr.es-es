---
title: DRV_FREE mensaje (Mmsystem.h)
description: Notifica al controlador que se está quitando de la memoria. El controlador debe liberar cualquier memoria y otros recursos del sistema que haya asignado.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a558dc7a2c3ece040790b2351ff39dc3054d660eb9368567ed7ce79d40c8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526215"
---
# <a name="drv_free-message"></a>Mensaje DRV \_ FREE

Notifica al controlador que se está quitando de la memoria. El controlador debe liberar cualquier memoria y otros recursos del sistema que haya asignado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

No se usan los parámetros *dwDriverId,* *lParam1* y *lParam2.*

El **mensaje DRV \_ FREE** siempre es el último que recibe un controlador de dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> <dt>

[Mensajes de controlador instalables](installable-driver-messages.md)
</dt> </dl>

 

 





