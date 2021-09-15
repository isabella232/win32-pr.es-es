---
description: Especifica el nombre de familia del paquete de aplicación para una aplicación de configuración de cámara virtual.
title: MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572756"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>Atributo MF \_ VIRTUALCAMERA \_ APP PACKAGE FAMILY \_ \_ \_ NAME

Especifica el nombre de familia del paquete de aplicación para una aplicación de configuración de cámara virtual. Cuando se proporciona, la canalización asociará la aplicación de configuración con la cámara virtual y proporcionará un punto de inicio dentro de la página de Configuración cámara.

## <a name="data-type"></a>Tipo de datos

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>Observaciones

El origen multimedia personalizado de la cámara virtual puede exponer este atributo desde el almacén de atributos de origen multimedia [IMFMediaSourceEx::GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource).  

Si la aplicación de configuración aún no está instalada en el equipo, se inicia la aplicación Store y se navega a la página de la aplicación especificada por el nombre de familia del paquete. De lo contrario, se inicia la aplicación instalada para el usuario.


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Compilación 22000<br/>                          |
| Servidor mínimo compatible<br/> | Windows Compilación 22000<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




