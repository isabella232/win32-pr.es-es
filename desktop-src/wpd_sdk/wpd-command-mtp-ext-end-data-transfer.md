---
description: El comando WPD COMMAND MTP EXT END DATA TRANSFER completa una transferencia de datos y \_ una respuesta de lectura desde el \_ \_ \_ \_ \_ dispositivo.
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466645"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>Comando DE WPD \_ \_ Comando MTP EXT END \_ DATA \_ \_ \_ TRANSFER

El **comando WPD \_ COMMAND \_ MTP EXT END DATA \_ \_ \_ \_ TRANSFER** completa una transferencia de datos y una respuesta de lectura desde el dispositivo. La transferencia se inicia mediante el comando [**WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) o el comando [**WPD COMMAND \_ \_ MTP EXT EXECUTE \_ CON DATA TO \_ \_ \_ \_ \_ \_ WRITE.**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write)

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR EXT DE MTP DE CATEGORÍA \_ \_ \_ WPD \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                      | VarType    | Descripción                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **CONTEXTO DE TRANSFERENCIA EXT \_ \_ DE MTP DE LA PROPIEDAD \_ \_ \_ WPD** | VT \_ LPWSTR | Necesario. Identifica el contexto devuelto por una llamada de método anterior. |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                        | VarType | Descripción                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE RESPUESTA EXT DE MTP DE LA PROPIEDAD \_ \_ \_ \_ \_ WPD**   | VT \_ UI4 | Required.El código de respuesta al código de operación del proveedor.                                                                                |
| **MTP \_ \_ EXT \_ \_ RESPONSE \_ PARAMS DE LA PROPIEDAD WPD** | VT \_ UI4 | Opcional. Colección **IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta. Esta colección puede estar vacía. |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con extensiones de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

