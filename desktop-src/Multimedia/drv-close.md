---
title: Mensaje de DRV_CLOSE (mmsystem. h)
description: Indica al controlador que cierre la instancia de especificada. Si no hay ninguna otra instancia abierta, el controlador debe prepararse para la versión posterior de la memoria.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- Mensaje de DRV_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a205b7e6edb4a427b0e80d32cc711d9bf2b052c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651420"
---
# <a name="drv_close-message"></a>DRV- \_ cerrar mensaje

Indica al controlador que cierre la instancia de especificada. Si no hay ninguna otra instancia abierta, el controlador debe prepararse para la versión posterior de la memoria.

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

32: valor de bit especificado como parámetro *lParam1* en una llamada a la función **DriverClose** .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32: valor de bit especificado como parámetro *lParam2* en una llamada a la función **DriverClose** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

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

 

 





