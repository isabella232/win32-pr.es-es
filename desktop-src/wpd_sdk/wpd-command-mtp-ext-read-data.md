---
description: El comando \_ WPD \_ \_ ext \_ Read data del comando de WPD \_ recupera los datos del dispositivo después de ejecutar el comando de la extensión de comandos de ejecución ext del comando WPD \_ \_ \_ \_ \_ \_ con \_ datos \_ para \_ leer.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Comando WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709027"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando de WPD comando \_ \_ \_ ext \_ Read \_ Data

El **comando \_ WPD \_ \_ ext \_ Read \_ Data del comando de WPD** recupera los datos del dispositivo después de ejecutar el comando de la extensión de comandos de ejecución ext del comando **WPD \_ \_ \_ \_ \_ \_ con \_ datos \_ para \_ leer** .

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                   | VarType             | Descripción                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **propiedad de WPD \_ \_ \_ contexto de transferencia ext de MTP \_ \_**              | VT \_ LPWStr          | Obligatorio. Identifica el contexto devuelto por la llamada anterior al dispositivo. |
| **\_propiedad \_ de WPD \_ \_ transferencia de ext. \_ número \_ de bytes \_ para \_ leer** | VT \_ UI4             | Obligatorio. Especifica el número de bytes que se van a leer.                                       |
| **propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**                 | VT \_ Vector \| VT \_ UI1 | Obligatorio. Identifica el búfer en el que se copian los datos del dispositivo.                  |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                  | VarType             | Descripción                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **propiedad de WPD \_ \_ transferencia de ext. número de \_ \_ \_ \_ bytes \_ leídos** | VT \_ UI4             | Obligatorio. Especifica el número de bytes recibidos del dispositivo. |
| **propiedad de WPD \_ \_ \_ datos de transferencia ext de MTP \_ \_**             | VT \_ Vector \| VT \_ UI1 | Obligatorio. Búfer que contiene los datos del dispositivo.               |



 

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

 

 




