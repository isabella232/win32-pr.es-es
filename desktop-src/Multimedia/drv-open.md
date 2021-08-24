---
title: DRV_OPEN mensaje (Mmsystem.h)
description: Dirige al controlador para que abra una nueva instancia.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 537d3067c85cf3f92eaf2fae81cd392490ff9fa728ed8377d8241c7204cf64e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691585"
---
# <a name="drv_open-message"></a>Mensaje DE \_ DRV OPEN

Dirige al controlador para que abra una nueva instancia.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador del controlador instalable.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador de la instancia del controlador instalable.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Dirección de una cadena de caracteres anchos terminada en NULL que especifica la información de configuración utilizada para abrir la instancia. Si no hay información de configuración disponible, esta cadena está vacía o el parámetro es **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Datos específicos del controlador de 32 bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero de lo contrario.

## <a name="remarks"></a>Comentarios

Si el controlador devuelve un valor distinto de cero, el sistema usa ese valor como identificador del controlador (el parámetro *dwDriverId)* en los mensajes que envía posteriormente a la instancia del controlador. El controlador puede devolver cualquier tipo de valor como identificador. Por ejemplo, algunos controladores devuelven direcciones de memoria que apuntan a información específica de la instancia. El uso de este método para especificar identificadores para una instancia de controlador proporciona a los controladores acceso listo a la información mientras están procesando mensajes.

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

 

 





