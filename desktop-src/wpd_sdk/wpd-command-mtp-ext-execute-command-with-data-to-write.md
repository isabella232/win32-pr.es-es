---
description: El comando WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir envía un bloque de comandos MTP, que va seguido de una fase de datos. Los datos se envían desde el host al dispositivo.
ms.assetid: b675fc3c-4d50-429d-9e00-42160d409a2b
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_WRITE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6f7c65cad838ded52471b5e0dd8dfad325fb1ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709034"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_write-command"></a>Comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir

El comando **WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ escribir** envía un bloque de comandos MTP, que va seguido de una fase de datos. Los datos se envían desde el host al dispositivo.

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                | VarType | Descripción                                                                                                                             |
|----------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**             | VT \_ UI4 | Obligatorio. Identifica un código de operación MTP extendido por un proveedor.                                                                              |
| **\_parámetros de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**           | VT \_ UI4 | Obligatorio. Una colección **IPortableDevicePropVariantCollection** que identifica los parámetros necesarios para el código de operación del proveedor. |
| **propiedad de WPD \_ \_ extensión de \_ \_ \_ datos totales de transferencia ext \_ MTP \_** | VT \_ UI8 | Requerido. especifica el tamaño total de los datos, en bytes, excluyendo cualquier sobrecarga que se envíe al dispositivo.                                         |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                       | VarType    | Descripción                                                                        |
|--------------------------------------------------------------|------------|------------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ tamaño de \_ \_ \_ búfer de transferencia óptimo \_ ext de \_ MTP** | VT \_ UI4    | Obligatorio. Especifica el tamaño óptimo del búfer de transferencia.                       |
| **propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**               | VT \_ LPWStr | Opcional. Identificador de contexto que utiliza el controlador para las transferencias de datos posteriores. |



 

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

 

 




