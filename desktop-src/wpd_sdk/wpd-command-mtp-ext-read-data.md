---
description: El comando WPD COMMAND MTP EXT READ DATA recupera datos del dispositivo después de ejecutar el comando \_ \_ \_ \_ \_ WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ READ.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5aeee37e1922f91e9a9fac7881369364d01340893829678a5651f89ed428440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927955"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando \_ \_ MTP \_ EXT \_ READ \_ DATA de WPD

El **comando WPD \_ COMMAND \_ MTP EXT READ \_ \_ \_ DATA** recupera datos del dispositivo después de ejecutar el comando **WPD COMMAND \_ \_ MTP EXT EXECUTE COMMAND \_ WITH DATA TO \_ \_ \_ \_ \_ \_ READ.**

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR EXT DE MTP DE CATEGORÍA \_ \_ \_ WPD \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                   | VarType             | Descripción                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **CONTEXTO DE TRANSFERENCIA EXT \_ \_ DE MTP DE LA PROPIEDAD \_ \_ \_ WPD**              | VT \_ LPWSTR          | Obligatorio. Identifica el contexto devuelto por la llamada anterior al dispositivo. |
| **MTP \_ EXT TRANSFER NUM BYTES TO \_ \_ \_ \_ \_ \_ \_ READ DE LA PROPIEDAD WPD** | VT \_ UI4             | Obligatorio. Especifica el número de bytes que se leerán.                                       |
| **DATOS DE \_ TRANSFERENCIA EXT \_ DE MTP DE LA \_ \_ PROPIEDAD WPD \_**                 | VT \_ VECTOR \| VT \_ UI1 | Obligatorio. Identifica el búfer en el que se copian los datos del dispositivo.                  |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                  | VarType             | Descripción                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **MTP \_ EXT TRANSFER NUM \_ \_ \_ \_ \_ BYTES \_ READ DE LA PROPIEDAD WPD** | VT \_ UI4             | Obligatorio. Especifica el número de bytes recibidos del dispositivo. |
| **DATOS DE \_ TRANSFERENCIA EXT \_ DE MTP DE LA \_ \_ PROPIEDAD WPD \_**             | VT \_ VECTOR \| VT \_ UI1 | Obligatorio. Búfer que contiene los datos del dispositivo.               |



 

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

 

 




