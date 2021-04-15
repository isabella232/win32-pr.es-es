---
description: El \_ comando de \_ WPD \_ \_ \_ de extensión de proveedor ext Get Vendor \_ Extension \_ Description recupera la cadena de descripción de extensión de proveedor. Esta cadena se define mediante un conjunto de DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Comando WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709028"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Comando de WPD comando \_ \_ \_ ext \_ get de \_ extensión de proveedor \_ \_

El comando de **WPD de \_ extensión de \_ \_ \_ proveedor ext Get \_ Vendor \_ Extension \_ Description** recupera la cadena de descripción de extensión de proveedor. Esta cadena se define mediante un conjunto de **DeviceInfo** .

## <a name="command-category"></a>Categoría de comando

**Categoría de WPD de \_ \_ \_ operaciones de proveedor ext MTP \_ \_**

## <a name="parameters"></a>Parámetros

Este comando no contiene parámetros.

## <a name="return-value"></a>Valor devuelto

El controlador devuelve los resultados siguientes.



| Resultado                                                      | VarType    | Descripción                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **propiedad de WPD \_ \_ \_ extensión del proveedor ext de MTP \_ \_ \_** | VT \_ LPWStr | Obligatorio. Especifica la cadena de descripción de la extensión de proveedor. |



 

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

 

 




