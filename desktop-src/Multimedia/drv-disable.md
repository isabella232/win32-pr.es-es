---
title: Mensaje de DRV_DISABLE (mmsystem. h)
description: Deshabilita el controlador. El controlador debe colocar el dispositivo correspondiente, si existe, en un estado inactivo y finalizar las funciones de devolución de llamada o los subprocesos.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- Mensaje de DRV_DISABLE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997092"
---
# <a name="drv_disable-message"></a>DRV \_ deshabilitar mensaje

Deshabilita el controlador. El controlador debe colocar el dispositivo correspondiente, si existe, en un estado inactivo y finalizar las funciones de devolución de llamada o los subprocesos.

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

Después de deshabilitar el controlador, el sistema normalmente envía un mensaje [**DRV \_ Free**](drv-free.md) al controlador antes de quitar el controlador de la memoria.

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

 

 





