---
description: El comando \_ WPD \_ \_ ext \_ End Data Transfer del comando WPD \_ \_ completa una transferencia de datos y lee la respuesta del dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: Comando WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709106"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>Comando de WPD comando \_ \_ \_ ext \_ End \_ Data \_ Transfer

El **comando \_ WPD \_ \_ ext \_ End \_ Data \_ transfer del comando WPD** completa una transferencia de datos y lee la respuesta del dispositivo. La transferencia se inicia con el comando [**WPD \_ ext Execute del comando de WPD \_ con los \_ \_ \_ \_ \_ datos \_ para \_ leer**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) , el comando o el comando de [**\_ \_ ext Execute MTP del comando de WPD \_ \_ \_ \_ con \_ datos \_ para \_ escribir**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) el comando.

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                      | VarType    | Descripción                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_** | VT \_ LPWStr | Obligatorio. Identifica el contexto devuelto por una llamada al método anterior. |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                        | VarType | Descripción                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ \_ respuesta ext \_ de MTP de propiedad de \_ WPD**   | VT \_ UI4 | Requerido. el código de respuesta para el código de operación del proveedor.                                                                                |
| **propiedad de WPD \_ \_ \_ parámetros de respuesta ext de MTP \_ \_** | VT \_ UI4 | Opcional. Colección **IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta. Esta colección puede estar vacía. |



 

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

 

