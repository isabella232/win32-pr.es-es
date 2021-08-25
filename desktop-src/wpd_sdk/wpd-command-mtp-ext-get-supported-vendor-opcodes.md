---
description: El comando \_ \_ MTP EXT GET SUPPORTED VENDOR OPCODES de WPD COMMAND envía \_ un bloque de comandos \_ \_ \_ \_ MTP. No hay ninguna fase de datos posterior asociada a este comando.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b0ab00fc3ada963e56dced49f97d3c1dbca578dfc5c1cded4735f9df947ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927975"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>COMANDO WPD \_ \_ MTP \_ EXT GET SUPPORTED VENDOR \_ \_ \_ \_ OPCODES Command

El **comando \_ \_ MTP \_ EXT GET SUPPORTED VENDOR \_ \_ \_ \_ OPCODES** de WPD COMMAND envía un bloque de comandos MTP. No hay ninguna fase de datos posterior asociada a este comando.

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR EXT DE MTP DE CATEGORÍA \_ \_ \_ WPD \_ \_**

## <a name="parameters"></a>Parámetros

Este comando no contiene parámetros.

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                | VarType | Descripción                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **CÓDIGOS DE OPERACIÓN \_ DEL \_ PROVEEDOR DE MTP EXT \_ DE LA \_ \_ PROPIEDAD \_ WPD** | VT \_ UI4 | Obligatorio. **IPortableDevicePropVariantCollection que** contiene todos los códigos de operación extendidos por el proveedor. |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con extensiones de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




