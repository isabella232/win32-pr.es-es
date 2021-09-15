---
description: El comando WPD COMMAND MTP EXT EXECUTE COMMAND WITH DATA TO READ envía un bloque de comandos \_ \_ \_ \_ \_ \_ \_ \_ MTP, que va \_ seguido de una fase de datos. (Los datos se envían desde el dispositivo al host).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466644"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>COMANDO WPD \_ \_ MTP EXT EXECUTE COMMAND WITH DATA TO READ (COMANDO MTP \_ EXT EXECUTE CON DATOS PARA \_ \_ \_ \_ \_ \_ LEER)

El **comando WPD \_ COMMAND \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO \_ \_ \_ \_ \_ \_ READ** envía un bloque de comandos MTP, que va seguido de una fase de datos. (Los datos se envían desde el dispositivo al host).

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR EXT DE MTP DE CATEGORÍA \_ \_ \_ WPD \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                      | VarType | Descripción                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE OPERACIÓN \_ \_ EXT DE MTP DE LA PROPIEDAD \_ \_ \_ WPD**   | VT \_ UI4 | Necesario. Identifica un código de operación MTP extendido por el proveedor.                                                                    |
| **MTP \_ \_ EXT \_ \_ OPERATION \_ PARAMS DE LA PROPIEDAD WPD** | VT \_ UI4 | Necesario. **IPortableDevicePropVariantCollection**, que identifica los parámetros necesarios para el código de operación del proveedor. |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                       | VarType    | Descripción                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TAMAÑO TOTAL DE DATOS DE TRANSFERENCIA EXT DE LA PROPIEDAD \_ \_ WPD MTP \_ \_ \_ \_ \_**     | VT \_ UI8    | Necesario. Devuelve el tamaño total de los datos, en bytes, excepto cualquier sobrecarga procedente del dispositivo. Si el dispositivo notifica un tamaño de datos desconocido (0xFFFFFFFF), el controlador debe llamar a **ReadData** repetidamente hasta que se reciba un fragmento corto. |
| **TAMAÑO ÓPTIMO DEL BÚFER DE TRANSFERENCIA DE \_ \_ MTP \_ EXT DE \_ LA \_ \_ PROPIEDAD \_ WPD** | VT \_ UI4    | Opcional. Devuelve el tamaño óptimo del búfer de transferencia.                                                                                                                                                                          |
| **CONTEXTO DE TRANSFERENCIA EXT \_ \_ DE MTP DE LA PROPIEDAD \_ \_ \_ WPD**               | VT \_ LPWSTR | Necesario. Especifica el identificador de contexto para las transferencias de datos posteriores.                                                                                                                                                           |



 

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

 

 




