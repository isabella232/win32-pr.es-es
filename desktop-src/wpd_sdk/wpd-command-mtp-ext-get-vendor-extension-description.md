---
description: El comando WPD \_ COMMAND \_ MTP \_ EXT GET VENDOR EXTENSION DESCRIPTION recupera la cadena de descripción de la extensión de \_ \_ \_ \_ proveedor. Esta cadena se define mediante un conjunto de datos DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31622676161065ec685640789bc51eef64165542a9ebe4c9367ea1a03195e7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193519"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Comando WPD \_ \_ MTP \_ EXT GET VENDOR EXTENSION DESCRIPTION \_ (COMANDO MTP EXT GET VENDOR EXTENSION \_ \_ \_ DESCRIPTION)

El **comando WPD \_ COMMAND \_ MTP EXT GET VENDOR \_ \_ EXTENSION \_ \_ \_ DESCRIPTION** recupera la cadena de descripción de la extensión de proveedor. Esta cadena se define mediante un conjunto **de datos DeviceInfo.**

## <a name="command-category"></a>Categoría de comando

**OPERACIONES DE PROVEEDOR \_ \_ EXT DE MTP \_ \_ DE CATEGORÍA WPD \_**

## <a name="parameters"></a>Parámetros

Este comando no contiene parámetros.

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los siguientes resultados.



| Resultado                                                      | VarType    | Descripción                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **DESCRIPCIÓN DE LA \_ EXTENSIÓN DEL PROVEEDOR DE \_ MTP EXT DE LA \_ \_ \_ PROPIEDAD \_ WPD** | VT \_ LPWSTR | Obligatorio. Especifica la cadena de descripción de la extensión del proveedor. |



 

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

 

 




