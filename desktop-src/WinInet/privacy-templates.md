---
title: Plantillas de privacidad (Wininet. h)
description: A continuación se muestran los niveles de privacidad que son equivalentes a las reglas de aceptación, aceptación condicional o no aceptación de cookies.
ms.assetid: d8dd9c12-b159-4f95-820e-521aeb1526bf
topic_type:
- apiref
api_name:
- PRIVACY_TEMPLATE_NO_COOKIES
- PRIVACY_TEMPLATE_HIGH
- PRIVACY_TEMPLATE_MEDIUM_HIGH
- PRIVACY_TEMPLATE_MEDIUM
- PRIVACY_TEMPLATE_MEDIUM_LOW
- PRIVACY_TEMPLATE_LOW
- PRIVACY_TEMPLATE_CUSTOM
- PRIVACY_TEMPLATE_ADVANCED
- PRIVACY_TEMPLATE_MAX
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9394068721920836f61871ca42471469fd4c592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493162"
---
# <a name="privacy-templates"></a>Plantillas de privacidad

A continuación se muestran los niveles de privacidad que son equivalentes a las reglas de aceptación, aceptación condicional o no aceptación de cookies. Estos niveles corresponden a los niveles de preferencias de privacidad establecidos en la pestaña privacidad de opciones de Internet. Consulte [privacidad en Internet Explorer 6](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) para obtener definiciones detalladas.

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**plantilla de privacidad \_ \_ sin \_ cookies**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Esto es lo mismo que **bloquear todas las cookies** en la barra deslizante de preferencias de privacidad en **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**plantilla de privacidad \_ \_ alta**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Esto es lo **mismo que en** la barra deslizante de preferencias de privacidad de **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**plantilla de privacidad \_ \_ media \_ alta**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Es lo mismo que **medio \_ alto** en la barra deslizante de preferencias de privacidad de **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**plantilla de privacidad \_ \_ mediana**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Es el mismo que el **medio** en la barra deslizante de preferencias de privacidad de **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**plantilla de privacidad \_ \_ media \_ baja** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Es lo mismo que **bajo** en la barra deslizante de preferencias de privacidad de **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**plantilla de privacidad \_ \_ baja**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Esto es lo mismo que **aceptar todas las cookies** en la barra deslizante de preferencias de privacidad en **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**plantilla de privacidad \_ \_ personalizada**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Definido por el usuario. Consulte [Cómo crear un archivo de importación de privacidad personalizado](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) para saber cómo establecer la configuración de privacidad personalizada.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**plantilla de privacidad \_ \_ avanzada**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Definido por el usuario. Las opciones avanzadas se establecen en el cuadro de diálogo **Configuración avanzada de privacidad** accesible desde la pestaña **privacidad** de **Opciones de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**plantilla de privacidad \_ \_ máxima**
</dt> <dd> <dl> <dt>

plantilla de privacidad \_ \_ baja
</dt> <dt>



Igual que **la \_ plantilla \_ de privacidad Low**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

