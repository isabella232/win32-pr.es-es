---
description: El comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer envía un bloque de comandos MTP, que va seguido de una fase de datos. (Los datos se envían desde el dispositivo al host).
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be0668f0adc312a63702c570c8818e61ba8f5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709035"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>Comando \_ de WPD comando \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer

El comando de **WPD comando \_ \_ \_ ext \_ Execute comando \_ \_ con \_ datos \_ para \_ leer** envía un bloque de comandos MTP, que va seguido de una fase de datos. (Los datos se envían desde el dispositivo al host).

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                      | VarType | Descripción                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD**   | VT \_ UI4 | Obligatorio. Identifica un código de operación MTP extendido por un proveedor.                                                                    |
| **\_parámetros de \_ \_ operación ext \_ de MTP de propiedad de \_ WPD** | VT \_ UI4 | Obligatorio. Un **IPortableDevicePropVariantCollection**, que identifica los parámetros necesarios para el código de operación del proveedor. |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                       | VarType    | Descripción                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ extensión de \_ \_ \_ datos totales de transferencia ext \_ MTP \_**     | VT \_ UI8    | Obligatorio. Devuelve el tamaño total de los datos, en bytes, excluyendo cualquier sobrecarga procedente del dispositivo. Si el dispositivo informa de un tamaño de campo desconocido (0xFFFFFFFF), el controlador debe llamar a **ReadData** repetidamente hasta que se reciba un fragmento breve. |
| **propiedad de WPD \_ \_ tamaño de \_ \_ \_ búfer de transferencia óptimo \_ ext de \_ MTP** | VT \_ UI4    | Opcional. Devuelve el tamaño óptimo del búfer de transferencia.                                                                                                                                                                          |
| **propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**               | VT \_ LPWStr | Obligatorio. Especifica el identificador de contexto para las transferencias de datos posteriores.                                                                                                                                                           |



 

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

 

 




