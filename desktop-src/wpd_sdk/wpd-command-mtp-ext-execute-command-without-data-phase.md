---
description: El comando de WPD comando \_ \_ \_ ext \_ Execute comando \_ sin la fase de \_ \_ datos \_ envía un bloque de comandos MTP. No hay ninguna fase de datos subsiguiente asociada a este comando.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: Comando WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b58648547c33206e1de19c14aea48427bc9db0be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709031"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>Comando de WPD comando \_ \_ \_ ext \_ Execute \_ comando \_ sin \_ fase de datos \_

El comando de **WPD comando \_ \_ \_ ext \_ Execute comando \_ sin la \_ \_ \_ fase de datos** envía un bloque de comandos MTP. No hay ninguna fase de datos subsiguiente asociada a este comando.

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



| Resultado                                        | VarType | Descripción                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **\_código de \_ \_ respuesta ext \_ de MTP de propiedad de \_ WPD**   | VT \_ UI4 | Obligatorio. Código de respuesta al código de operación del proveedor.                                                                      |
| **propiedad de WPD \_ \_ \_ parámetros de respuesta ext de MTP \_ \_** | VT \_ UI4 | Opcional. **IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta. Esta colección puede estar vacía. |



 

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

 

 




