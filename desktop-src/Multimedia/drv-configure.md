---
title: DRV_CONFIGURE mensaje (Mmsystem.h)
description: Dirige al controlador instalable para que muestre su cuadro de diálogo de configuración y permita al usuario especificar una nueva configuración para la instancia de controlador instalable dada.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- DRV_CONFIGURE mensaje Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370441"
---
# <a name="drv_configure-message"></a>MENSAJE DE CONFIGURACIÓN DE DRV \_

Dirige al controlador instalable para que muestre su cuadro de diálogo de configuración y permita al usuario especificar una nueva configuración para la instancia de controlador instalable dada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador del controlador instalable. Este es el mismo valor devuelto anteriormente por el controlador del [**mensaje DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador de la ventana primaria. Esta ventana se usa como ventana primaria para el cuadro de diálogo de configuración.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Dirección de una [**estructura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **NULL.** Si se da la estructura , contiene los nombres de la clave del Registro y el valor asociados al controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos valores:



| Requisito | Value |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | La configuración es correcta; no se requiere ninguna otra acción.                                    |
| DRVCNF \_ CANCEL  | El usuario canceló el cuadro de diálogo; no se requiere ninguna otra acción.                                   |
| REINICIO \_ DRVCNF | La configuración es correcta, pero los cambios no se hacen efectivos hasta que se reinicia el sistema. |



 

## <a name="remarks"></a>Observaciones

Algunos controladores instalables anexan información de configuración al valor asignado al valor del Registro asociado al controlador.

Los valores devueltos DRV CANCEL, DRV OK y DRV RESTART están obsoletos; se han reemplazado por \_ \_ \_ DRVCNF \_ CANCEL, DRVCNF OK y \_ DRVCNF \_ RESTART, respectivamente.

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

 

