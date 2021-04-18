---
description: El comando de la \_ extensión de datos de escritura MTP de comando de WPD \_ \_ \_ \_ envía datos al dispositivo después de ejecutar el comando WPD \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Comando WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709026"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>Comando de WPD comando \_ \_ \_ ext \_ Write \_ Data

El comando de la **\_ extensión de \_ \_ \_ \_ datos de escritura MTP de comando de WPD** envía datos al dispositivo después de ejecutar el comando **WPD \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir** .

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                    | VarType             | Descripción                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**               | VT \_ LPWStr          | Obligatorio. Identifica el contexto devuelto por la llamada anterior al dispositivo. |
| **\_propiedad \_ de WPD \_ \_ transferencia de ext. \_ número \_ de bytes \_ que se van a \_ escribir** | VT \_ UI4             | Obligatorio. Especifica el número de bytes que se van a escribir.                                      |
| **propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**                  | VT \_ Vector \| VT \_ UI1 | Obligatorio. Identifica el búfer en el que se copian los datos del dispositivo.                  |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                     | VarType | Descripción                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **propiedad de WPD \_ \_ transferencia de ext. número de \_ \_ \_ \_ bytes \_ escritos** | VT \_ UI4 | Obligatorio. Especifica el número de bytes enviados al dispositivo.. |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




