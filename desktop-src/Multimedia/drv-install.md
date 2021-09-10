---
title: DRV_INSTALL mensaje (Mmsystem.h)
description: Notifica al controlador que se está instalando. El controlador debe crear e inicializar las claves y los valores del Registro necesarios y comprobar que los controladores y el hardware compatibles están instalados y configurados correctamente.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- DRV_INSTALL mensaje Windows multimedia
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370471"
---
# <a name="drv_install-message"></a>Mensaje DRV \_ INSTALL

Notifica al controlador que se está instalando. El controlador debe crear e inicializar las claves y los valores del Registro necesarios y comprobar que los controladores y el hardware compatibles están instalados y configurados correctamente.

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

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Dirección de una [**estructura DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) o **NULL.** Si se da una estructura, contiene los nombres de la clave del Registro y el valor asociados al controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de estos valores:



| Requisito | Value |
|-----------------|--------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | La instalación se realiza correctamente; no se requiere ninguna otra acción.                             |
| DRVCNF \_ CANCEL  | Error de instalación.                                                                  |
| REINICIO \_ DRVCNF | La instalación se realiza correctamente, pero no se realiza hasta que se reinicia el sistema. |



 

## <a name="remarks"></a>Observaciones

No se usa el parámetro *lParam1.*

Algunos controladores instalables anexan información de configuración al valor asignado al valor del Registro asociado al controlador.

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

 

