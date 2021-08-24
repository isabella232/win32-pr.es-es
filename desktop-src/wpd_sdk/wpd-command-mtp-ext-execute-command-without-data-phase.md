---
description: El comando WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITHOUT DATA PHASE envía un bloque de comandos \_ \_ \_ \_ \_ MTP. No hay ninguna fase de datos subsiguiente asociada a este comando.
ms.assetid: 308550d0-1399-4b64-8f8e-dc16d5044086
title: WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITHOUT_DATA_PHASE (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c4d1d5af4d1e4e712f3a39dd5cbb296133bb16f4de3b677da4a45fa7bbc204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806305"
---
# <a name="wpd_command_mtp_ext_execute_command_without_data_phase-command"></a>COMANDO WPD \_ \_ COMANDO MTP EXT EXECUTE \_ COMMAND WITHOUT DATA PHASE \_ \_ \_ \_ \_ Command

El **comando WPD \_ COMMAND \_ MTP EXT EXECUTE COMMAND \_ WITHOUT DATA \_ \_ \_ \_ \_ PHASE** envía un bloque de comandos MTP. No hay ninguna fase de datos subsiguiente asociada a este comando.

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR EXT DE MTP DE CATEGORÍA \_ \_ WPD \_ \_ \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                      | VarType | Descripción                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE OPERACIÓN \_ \_ EXT DE MTP DE LA \_ \_ PROPIEDAD \_ WPD**   | VT \_ UI4 | Obligatorio. Identifica un código de operación MTP extendido por el proveedor.                                                                    |
| **MTP \_ \_ EXT \_ \_ OPERATION \_ PARAMS DE LA PROPIEDAD WPD** | VT \_ UI4 | Obligatorio. **IPortableDevicePropVariantCollection**, que identifica los parámetros necesarios para el código de operación del proveedor. |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los siguientes resultados.



| Resultado                                        | VarType | Descripción                                                                                                                    |
|-----------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------|
| **CÓDIGO DE RESPUESTA \_ \_ EXT DE MTP DE LA \_ \_ PROPIEDAD \_ WPD**   | VT \_ UI4 | Obligatorio. Código de respuesta al código de operación del proveedor.                                                                      |
| **MTP \_ \_ EXT \_ \_ RESPONSE \_ PARAMS DE LA PROPIEDAD WPD** | VT \_ UI4 | Opcional. **IPortableDevicePropVariantCollection** que identifica los parámetros de respuesta. Esta colección puede estar vacía. |



 

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

 

 




