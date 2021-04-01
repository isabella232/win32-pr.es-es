---
title: Mensaje de DRV_ENABLE (mmsystem. h)
description: Habilita el controlador. El controlador debe inicializar las variables y ubicar los dispositivos con la interfaz de entrada y salida (e/s).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- Mensaje de DRV_ENABLE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997094"
---
# <a name="drv_enable-message"></a>DRV- \_ Habilitar mensaje

Habilita el controlador. El controlador debe inicializar las variables y ubicar los dispositivos con la interfaz de entrada y salida (e/s).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No se usan los parámetros *dwDriverId*, *lParam1* y *lParam2* .

Los controladores se consideran habilitados desde el momento en que reciben este mensaje hasta que se deshabiliten mediante el mensaje [**DRV \_ Disable**](drv-disable.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Controladores instalables](installable-drivers.md)
</dt> <dt>

[Mensajes de controlador instalables](installable-driver-messages.md)
</dt> </dl>

 

 





