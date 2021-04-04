---
description: En este tema se describe cómo puede trabajar con nombres de dominio internacionalizados (IDN) en sus aplicaciones.
ms.assetid: e0ca356e-f8c1-4845-ae1e-ce2ae8987515
title: Administrar nombres de dominio internacionalizados (IDN)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95e853f0ea3f62fc3e5ee848431417cc031eaa5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277753"
---
# <a name="handling-internationalized-domain-names-idns"></a>Administrar nombres de dominio internacionalizados (IDN)

En este tema se describe cómo puede trabajar con nombres de dominio internacionalizados (IDN) en sus aplicaciones. Los IDN se especifican mediante el grupo de trabajo [de red RFC 3490: internacionalización de nombres de dominio en las aplicaciones (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). Antes de este borrador estándar, los IDN se limitaban a los caracteres latinos sin diacríticos. IDNA permite a IDN incluir caracteres latinos con signos diacríticos, junto con caracteres de scripts no latinos, como cirílico, Árabe y chino. El estándar también establece reglas para asignar IDN a nombres de dominio solo ASCII. Por lo tanto, se pueden controlar los problemas de IDNA en el lado cliente, sin necesidad de realizar cambios en el servidor de nombres de dominio (DNS).

> [!Caution]  
> RFC 3490 presenta una serie de problemas de seguridad relacionados con el uso de IDN. Para obtener más información, vea la sección relacionada de [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

> [!Note]  
> IDNA se basa actualmente en Unicode 3,2.

 

## <a name="nls-api-functions-for-handling-idns"></a>NLS API funciones para controlar IDN

NLS incluye las siguientes funciones de conversión que la aplicación puede usar para convertir un IDN en representaciones diferentes. Para obtener un ejemplo del uso de estas funciones, vea [NLS: ejemplo de conversión de nombres de dominio internacionalizados (IDN)](nls--internationalized-domain-name--idn--conversion-sample.md).

-   [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii). Convierte un IDN en Punycode.
-   [**IdnToNameprepUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntonameprepunicode). Realiza la parte NamePrep de la conversión de un IDN en un nombre ASCII. Esta función crea una representación canónica de Unicode de una cadena.
-   [**IdnToUnicode**](/windows/desktop/api/Winnls/nf-winnls-idntounicode). Convierte una cadena Punycode en una cadena UTF-16 normal.

NLS también define varias funciones de API que se pueden usar para mitigar algunos de los riesgos de seguridad presentados por la tecnología IDN. En Windows Vista y versiones posteriores, se usan las siguientes funciones para comprobar que los caracteres de un IDN determinado se dibujan completamente a partir de los scripts asociados a una configuración regional o configuraciones regionales determinadas. Para obtener un ejemplo del uso de estas funciones, vea [NLS: ejemplo de mitigación de nombres de dominio internacionalizados (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md).

-   [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts). Proporciona una lista de los scripts usados en una cadena determinada.
-   [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa), [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex). Recuperar información de configuración regional. El uso de las funciones con *LCType* establecido en [configuración regional \_ SSCRIPTS](locale-sscripts.md) proporciona una lista de los scripts que se suelen usar para una configuración regional concreta.
-   [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts). Compara listas de scripts. Para comprobarlo con varias configuraciones regionales, la aplicación puede realizar varias llamadas a [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o a [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) y [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

En el caso de las aplicaciones que se ejecutan en Windows XP y Windows Server 2003, las funciones [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md), [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)y [**DownlevelVerifyScripts**](downlevelverifyscripts.md) desempeñan un papel similar al de las funciones enumeradas anteriormente en mitigar el riesgo de seguridad. La descarga ["API de mitigación de nombres de dominio internacionalizados (IDN)" de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) está disponible en el [centro de descarga de MSDN](https://www.microsoft.com/?ref=go).

## <a name="handle-unicode-strings"></a>Administrar cadenas Unicode

IDNA admite la transformación de cadenas Unicode en etiquetas de nombre de host legítimas, con la excepción de cadenas que contienen ciertos caracteres prohibidos, como caracteres de control, caracteres del área de uso privado (PUA) y similares. La aplicación puede usar la \_ marca IDN use \_ STD3 \_ ASCII \_ rules con varias funciones de conversión de NLS para forzar que las funciones generen un error si encuentran caracteres ASCII distintos de letras, números o guiones (-), o si una cadena comienza o termina con el carácter de guión menos. Siempre se prohíbe el uso de estos caracteres en los nombres de dominio y permanecen prohibidos en el borrador estándar.

## <a name="handle-unassigned-code-points"></a>Administrar puntos de código sin asignar

IDN no puede contener puntos de código sin asignar. Por lo tanto, los puntos de código que no están asociados a un carácter ("asignado") a partir de Unicode 3,2 no tienen asignaciones de IDN definidas, aunque la marca IDN permitir la asignación \_ \_ sin asignar en ciertas funciones de conversión permite que se asignen a Punycode. Puede encontrar una lista de puntos de código sin asignar en [RFC 3454](http://www.faqs.org/rfcs/rfc3454.html).

> [!Caution]  
> Si la aplicación codifica puntos de código sin asignar como Punycode, los nombres de dominio resultantes no deben ser válidos. La seguridad puede verse comprometida si una versión posterior de IDNA hace que estos nombres sean válidos o si la aplicación filtra los caracteres no válidos para intentar crear un nombre de dominio válido.

 

No se permiten puntos de código sin asignar en las cadenas almacenadas que se usan en los identificadores de protocolo y entidades con nombre, como los nombres de los certificados digitales y las partes del nombre de dominio DNS. Sin embargo, los puntos de código se permiten en las cadenas de consulta, por ejemplo, los nombres especificados por el usuario para las entidades de certificación digitales y las búsquedas de DNS, que se usan para hacer coincidir con los identificadores almacenados.

> [!Caution]  
> Aunque las cadenas de consulta pueden usar puntos de código sin asignar, no deben usarse en las aplicaciones. Incluso una cadena de consulta proporcionada por el usuario presenta un riesgo de un ataque de suplantación de identidad. En este tipo de ataque, el sitio host no escrupuloso vuelve a enrutar a los usuarios desde el sitio al que pretenden acceder a otro sitio que podría proporcionar información confidencial a terceros. Por ejemplo, la copia de una cadena de un correo electrónico entrante puede presentar los mismos riesgos que hacer clic en un vínculo de un explorador.

 

## <a name="convert-domain-names-to-ascii-names"></a>Convertir nombres de dominio en nombres ASCII

La aplicación puede usar la función [**IdnToAscii**](/windows/desktop/api/Winnls/nf-winnls-idntoascii) y ciertas funciones de mitigación para convertir IDN en ASCII.

> [!Caution]  
> Dado que las cadenas con representaciones binarias muy diferentes se pueden comparar como idénticas, esta función puede generar determinados problemas de seguridad. Para obtener más información, vea la explicación de las funciones de comparación en [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

 

## <a name="examples"></a>Ejemplos

[NLS: el ejemplo de conversión de nombres de dominio internacionalizados (IDN)](nls--internationalized-domain-name--idn--conversion-sample.md) muestra el uso de las funciones de conversión de IDN. [NLS: el ejemplo de mitigación de nombres de dominio internacionalizados (IDN)](nls--internationalized-domain-name--idn--mitigation-sample.md) muestra el uso de las funciones de mitigación de IDN.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la compatibilidad con National Language](using-national-language-support.md)
</dt> <dt>

[Consideraciones de seguridad: características internacionales](security-considerations--international-features.md)
</dt> </dl>

 

 



