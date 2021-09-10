---
title: DRV_DISABLE mensaje (Mmsystem.h)
description: Deshabilita el controlador. El controlador debe colocar el dispositivo correspondiente, si lo hay, en un estado inactivo y finalizar las funciones o subprocesos de devolución de llamada.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370460"
---
# <a name="drv_disable-message"></a>Mensaje DISABLE de DRV \_

Deshabilita el controlador. El controlador debe colocar el dispositivo correspondiente, si lo hay, en un estado inactivo y finalizar las funciones o subprocesos de devolución de llamada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No se usan los parámetros *dwDriverId,* *lParam1* y *lParam2.*

Después de deshabilitar el controlador, el sistema normalmente envía al controlador un mensaje [**DRV \_ FREE**](drv-free.md) antes de quitarlo de la memoria.

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

 

 





