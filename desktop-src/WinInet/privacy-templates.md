---
title: Plantillas de privacidad (Wininet.h)
description: Los siguientes son niveles de privacidad que equivalen a las reglas para aceptar, aceptar condicionalmente o no aceptar cookies.
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
ms.openlocfilehash: 481aa3e9b6b5b5519bac6e458de1acba90f2cfa20dd0a5babac016d0003c70b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955565"
---
# <a name="privacy-templates"></a>Plantillas de privacidad

Los siguientes son niveles de privacidad que equivalen a las reglas para aceptar, aceptar condicionalmente o no aceptar cookies. Estos niveles corresponden a los niveles de preferencias de privacidad establecidos en la pestaña Privacidad de Opciones de Internet. Consulte [Privacidad en Internet Explorer 6 para](https://www.bing.com/search?q=Privacy+in+Internet+Explorer+6) obtener definiciones detalladas.

<dl> <dt>

<span id="PRIVACY_TEMPLATE_NO_COOKIES"></span><span id="privacy_template_no_cookies"></span>**PLANTILLA DE \_ PRIVACIDAD \_ SIN \_ COOKIES**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Esto es lo mismo que Bloquear todas las **cookies en** la barra deslizante Preferencias de privacidad en Opciones **de Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_HIGH"></span><span id="privacy_template_high"></span>**PLANTILLA \_ DE PRIVACIDAD \_ ALTA**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Esto es lo mismo que **Alto en la** barra deslizante Preferencias de privacidad en Opciones de **Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_HIGH"></span><span id="privacy_template_medium_high"></span>**PLANTILLA \_ DE PRIVACIDAD MEDIA \_ \_ ALTA**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Esto es lo mismo que **Medium \_ High en la** barra deslizante Preferencias de privacidad en Opciones de **Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM"></span><span id="privacy_template_medium"></span>**MEDIO DE \_ PLANTILLA DE \_ PRIVACIDAD**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Esto es lo mismo que **Medium en la** barra deslizante Preferencias de privacidad en Opciones de **Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MEDIUM_LOW_"></span><span id="privacy_template_medium_low_"></span>**PLANTILLA \_ DE PRIVACIDAD MEDIA \_ \_ BAJA** 
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Esto es lo mismo que **Baja en la** barra deslizante Preferencias de privacidad en Opciones de **Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_LOW"></span><span id="privacy_template_low"></span>**PLANTILLA \_ DE PRIVACIDAD \_ BAJA**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Esto es lo mismo que Aceptar todas **las cookies en** la barra deslizante Preferencias de privacidad en Opciones de **Internet.**


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_CUSTOM"></span><span id="privacy_template_custom"></span>**PLANTILLA \_ DE PRIVACIDAD \_ PERSONALIZADA**
</dt> <dd> <dl> <dt>

100
</dt> <dt>



Definido por el usuario. Consulte How to Create a Custom Privacy Import File (Cómo crear [un archivo de importación de privacidad personalizado)](https://www.bing.com/search?q=How+to+Create+a+Customized+Privacy+Import+File) para saber cómo establecer la configuración de privacidad personalizada.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_ADVANCED"></span><span id="privacy_template_advanced"></span>**PLANTILLA \_ DE PRIVACIDAD \_ AVANZADA**
</dt> <dd> <dl> <dt>

101
</dt> <dt>



Definido por el usuario. Las opciones avanzadas se establecen en el **cuadro de diálogo Configuración** privacidad avanzada accesible desde la **pestaña** Privacidad de Opciones **de Internet**.


</dt> </dl> </dd> <dt>

<span id="PRIVACY_TEMPLATE_MAX"></span><span id="privacy_template_max"></span>**PLANTILLA \_ DE PRIVACIDAD \_ MÁX.**
</dt> <dd> <dl> <dt>

PLANTILLA \_ DE PRIVACIDAD \_ BAJA
</dt> <dt>



Igual que **PRIVACY \_ TEMPLATE \_ LOW**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Wininet.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivacyGetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[**PrivacySetZonePreferenceW**](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

