---
description: El comando WPD COMMAND MTP EXT EXECUTE COMMAND WITH DATA TO WRITE envía un bloque de comandos \_ \_ \_ \_ \_ \_ \_ \_ \_ MTP, que va seguido de una fase de datos. Los datos se envían desde el host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ae0e50ad2fad9967252d9a21c1e864d056338a3e3a2b82f4c29d951a722953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806315"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>COMANDO WPD \_ \_ MTP EXT EXECUTE COMMAND WITH DATA TO WRITE (COMANDO MTP \_ EXT EXECUTE CON DATOS PARA \_ \_ \_ \_ \_ \_ ESCRIBIR)

El **comando WPD \_ COMMAND \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE** envía un bloque de comandos MTP, que va seguido de una fase de datos. Los datos se envían desde el host al dispositivo.

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR \_ \_ EXT DE MTP \_ \_ DE CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                | VarType | Descripción                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE OPERACIÓN \_ \_ EXT DE MTP DE LA \_ \_ PROPIEDAD \_ WPD**             | VT \_ UI4 | Obligatorio. Identifica un código de operación MTP extendido por el proveedor.                                                                              |
| **MTP \_ \_ EXT \_ \_ OPERATION \_ PARAMS DE LA PROPIEDAD WPD**           | VT \_ UI4 | Obligatorio. Colección **IPortableDevicePropVariantCollection** que identifica los parámetros necesarios para el código de operación del proveedor. |
| **TAMAÑO TOTAL DE DATOS DE TRANSFERENCIA EXT DE LA PROPIEDAD \_ \_ WPD MTP \_ \_ \_ \_ \_** | VT \_ UI8 | Required.Especifica el tamaño total de los datos, en bytes, sin incluir la sobrecarga, que se va a enviar al dispositivo.                                         |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los siguientes resultados.



| Resultado                                                       | VarType    | Descripción                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **TAMAÑO ÓPTIMO DEL BÚFER DE TRANSFERENCIA DE LA PROPIEDAD \_ \_ WPD MTP \_ EXT \_ \_ \_ \_** | VT \_ UI4    | Obligatorio. Especifica el tamaño óptimo del búfer de transferencia.                       |
| **CONTEXTO DE TRANSFERENCIA \_ \_ EXT DE MTP DE LA \_ \_ PROPIEDAD \_ WPD**               | VT \_ LPWSTR | Opcional. Identificador de contexto que el controlador usa para las transferencias de datos posteriores. |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




