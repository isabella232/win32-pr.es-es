---
description: El comando WPD COMMAND MTP EXT WRITE DATA envía datos al dispositivo después de ejecutar el comando \_ \_ \_ \_ \_ WPD \_ COMMAND \_ MTP \_ EXT EXECUTE COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467044"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>Comando \_ \_ MTP \_ EXT \_ WRITE \_ DATA de WPD

El **comando WPD \_ COMMAND \_ MTP EXT WRITE \_ \_ \_ DATA** envía datos al dispositivo después de ejecutar el comando **WPD COMMAND \_ \_ MTP EXT EXECUTE \_ COMMAND WITH DATA TO \_ \_ \_ \_ \_ \_ WRITE.**

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR \_ \_ EXT DE MTP \_ \_ DE CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

El controlador espera los parámetros siguientes.



| Parámetro                                                    | VarType             | Descripción                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **CONTEXTO DE TRANSFERENCIA \_ \_ EXT DE MTP DE LA \_ \_ PROPIEDAD \_ WPD**               | VT \_ LPWSTR          | Necesario. Identifica el contexto devuelto por la llamada anterior al dispositivo. |
| **BYTES \_ NUMÉRICOS DE TRANSFERENCIA EXT DE LA PROPIEDAD \_ WPD MTP \_ \_ PARA \_ \_ \_ \_ ESCRIBIR** | VT \_ UI4             | Necesario. Especifica el número de bytes que se escribirán.                                      |
| **PROPIEDAD WPD \_ \_ MTP \_ EXT TRANSFER \_ \_ DATA**                  | VT \_ VECTOR \| VT \_ UI1 | Necesario. Identifica el búfer en el que se copian los datos del dispositivo.                  |



 

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los siguientes resultados.



| Resultado                                                     | VarType | Descripción                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **BYTES \_ NUMÉRICOS DE TRANSFERENCIA EXT DE MTP DE LA PROPIEDAD WPD \_ \_ \_ \_ \_ \_ ESCRITOS** | VT \_ UI4 | Necesario. Especifica el número de bytes enviados al dispositivo. |



 

## <a name="calling-methods"></a>Llamar a métodos

Solo se puede llamar directamente mediante [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WpdMtpExtensions.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




