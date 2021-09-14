---
description: En este tema se describe cómo puede trabajar con nombres de dominio internacionalizados (IDN) en las aplicaciones.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Control de nombres de dominio internacionalizados (IDN)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063132"
---
# <a name="handling-internationalized-domain-names-idns"></a>Control de nombres de dominio internacionalizados (IDN)

En este tema se describe cómo puede trabajar con nombres de dominio internacionalizados (IDN) en las aplicaciones. Los IDN se especifican mediante el grupo de trabajo de red [RFC 3490: Internacionalización de](http://www.faqs.org/rfcs/rfc3490.html)nombres de dominio en aplicaciones (IDNA). Antes de este borrador de estándar, los IDN se limitaban a caracteres latinos sin signos diacríticos. IDNA permite que los IDN incluyan caracteres latinos con signos diacríticos, junto con caracteres de scripts no latinos, como cirílico, árabe y chino. El estándar también establece reglas para asignar identificadores a nombres de dominio solo ASCII. Por lo tanto, los problemas de IDNA se pueden controlar en el lado cliente, sin necesidad de realizar cambios en el servidor de nombres de dominio (DNS).

> [!Caution]  
> RFC 3490 presenta una serie de problemas de seguridad relacionados con el uso de IDN. Para obtener más información, vea la sección relacionada de [Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md).

 

> [!Note]  
> IdNA se basa actualmente en Unicode 3.2.

 

## <a name="nls-api-functions-for-handling-idns"></a>NLS API funciones para controlar los IDN

NLS incluye las siguientes funciones de conversión que la aplicación puede usar para convertir un IDN en diferentes representaciones. Para obtener un ejemplo del uso de estas funciones, vea [NLS: Internationalized Domain Name (IDN) Conversion Sample](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Convierte un IDN en Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Realiza la parte NamePrep de la conversión de un IDN a un nombre ASCII. Esta función crea una representación Unicode canónica de una cadena.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Convierte una cadena punycode en una cadena UTF-16 normal.

NLS también define varias funciones de API que se pueden usar para mitigar algunos de los riesgos de seguridad presentados por la tecnología IDN. En Windows Vista y versiones posteriores, se usan las siguientes funciones para comprobar que los caracteres de un IDN determinado se extraen completamente de los scripts asociados a una configuración regional o configuraciones regionales determinadas. Para obtener un ejemplo del uso de estas funciones, vea NLS: Ejemplo de mitigación de nombres de dominio [internacionalizados (IDN).](nls--internationalized-domain-name--idn--mitigation-sample.md)

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Proporciona una lista de scripts usados en una cadena determinada.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Recuperar información de configuración regional. El uso de las funciones *con LCType* establecido en [LOCALE \_ SSCRIPTS](locale-sscripts.md) proporciona una lista de scripts que se usan normalmente para una configuración regional determinada.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Compara listas de scripts. Para comprobar con varias configuraciones regionales, la aplicación puede realizar varias llamadas a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) y [**VerifyScripts.**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)

En el caso de las aplicaciones que se ejecutan en Windows XP y Windows Server 2003, las funciones [**DownlevelGetLocaleScripts,**](downlevelgetlocalescripts.md) [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)y [**DownlevelVerifyScripts**](downlevelverifyscripts.md) desempeñan un rol similar al de las funciones enumeradas anteriormente en mitigación del riesgo de seguridad. La descarga "Api de mitigación de nombres de dominio [internacionalizados (IDN) de Microsoft"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) está disponible en el Centro [de descarga de MSDN.](https://www.microsoft.com/?ref=go)

## <a name="handle-unicode-strings"></a>Controlar cadenas Unicode

IDNA admite la transformación de cadenas Unicode en etiquetas de nombre de host legítimas, a excepción de cadenas que contienen determinados caracteres prohibidos, como caracteres de control, caracteres del área de uso privado (PUA) y otros. La aplicación puede usar la marca IDN USE STD3 ASCII RULES con varias funciones de conversión NLS para forzar que las funciones no funcionen si encuentran caracteres ASCII distintos de letras, números o el carácter de guion menos \_ (-), o si una cadena comienza o termina con el carácter de guion \_ \_ \_ menos. Siempre se ha prohibido el uso de estos caracteres en los nombres de dominio y siguen estando prohibidos en el borrador del estándar.

## <a name="handle-unassigned-code-points"></a>Controlar puntos de código sin signo

Los IDN no pueden contener puntos de código sin signo. Por lo tanto, los puntos de código que no están asociados a un carácter ("asignado") a partir de Unicode 3.2 no tienen asignaciones de IDN definidas, aunque la marca IDN ALLOW UNASSIGNED en determinadas funciones de conversión permite asignarlas a \_ \_ Punycode. Puede encontrar una lista de puntos de código sin signo [en RFC 3454.](http://www.faqs.org/rfcs/rfc3454.html)

> [!Caution]  
> Si la aplicación codifica puntos de código sin signo como Punycode, los nombres de dominio resultantes no deberían ser válidos. La seguridad se puede poner en peligro si una versión posterior de IDNA hace que estos nombres sean válidos o si la aplicación filtra los caracteres no válidos para intentar crear un nombre de dominio legal.

 

No se permiten puntos de código sin asignar en las cadenas almacenadas usadas en identificadores de protocolo y entidades con nombre, como nombres en certificados digitales y elementos de nombre de dominio DNS. Sin embargo, los puntos de código se permiten en cadenas de consulta, por ejemplo, nombres escritos por el usuario para las autoridades de certificados digitales y las búsquedas DNS, que se usan para buscar coincidencias con identificadores almacenados.

> [!Caution]  
> Aunque las cadenas de consulta pueden usar puntos de código sin signo, no debe usarlos en las aplicaciones. Incluso una cadena de consulta proporcionada por el usuario presenta el riesgo de un ataque de "suplantación". En este tipo de ataque, el sitio host sin escrúpulos redirige a los usuarios desde el sitio al que pretenden acceder a otro sitio que podría proporcionar información confidencial a un tercero. Por ejemplo, copiar una cadena de un correo electrónico entrante puede presentar los mismos riesgos que hacer clic en un vínculo en un explorador.

 

## <a name="convert-domain-names-to-ascii-names"></a>Convertir nombres de dominio en nombres ASCII

La aplicación puede usar la [**función IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) y ciertas funciones de mitigación para convertir los IDN a ASCII.

> [!Caution]  
> Dado que las cadenas con representaciones binarias muy diferentes se pueden comparar como idénticas, esta función puede generar ciertos problemas de seguridad. Para obtener más información, vea la explicación de las funciones de comparación en [Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md).

 

## <a name="examples"></a>Ejemplos

NLS: Ejemplo de conversión de nombre de dominio [internacionalizado (IDN)](nls--internationalized-domain-name--idn--conversion-sample.md) muestra el uso de las funciones de conversión de IDN. [NLS: Ejemplo de mitigación de nombres de dominio internacionalizados (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md) muestra el uso de las funciones de mitigación de IDN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
</dt> <dt>

[Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md)
</dt> </dl>

 

 



