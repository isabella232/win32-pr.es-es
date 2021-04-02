---
title: Mensaje de DRV_CONFIGURE (mmsystem. h)
description: Dirige el controlador instalable para mostrar su cuadro de diálogo de configuración y permitir que el usuario especifique la nueva configuración para la instancia de controlador instalable especificada.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Mensaje de DRV_CONFIGURE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997093"
---
# <a name="drv_configure-message"></a>DRV \_ configurar mensaje

Dirige el controlador instalable para mostrar su cuadro de diálogo de configuración y permitir que el usuario especifique la nueva configuración para la instancia de controlador instalable especificada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador del controlador instalable. Este es el mismo valor que el controlador devolvió previamente desde el mensaje [**\_ abierto DRV**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador de la ventana primaria. Esta ventana se utiliza como ventana primaria para el cuadro de diálogo de configuración.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Dirección de una estructura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **null**. Si se proporciona la estructura, contiene los nombres de la clave del registro y el valor asociado al controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos valores:



| Requisito | Value |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ Aceptar      | La configuración es correcta; no es necesario realizar ninguna otra acción.                                    |
| \_Cancelar DRVCNF  | El usuario canceló el cuadro de diálogo. no es necesario realizar ninguna otra acción.                                   |
| reinicio de DRVCNF \_ | La configuración es correcta, pero los cambios no surten efecto hasta que se reinicia el sistema. |



 

## <a name="remarks"></a>Observaciones

Algunos controladores instalables anexan información de configuración al valor asignado al valor del registro asociado al controlador.

Los \_ valores de devolución DRV CANCEL, DRV \_ OK y DRV \_ restart son obsoletos; se han sustituido por DRVCNF \_ Cancel, DRVCNF \_ OK y DRVCNF \_ restart, respectivamente.

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

 

