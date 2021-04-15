---
description: El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos occidentales convencionales que se usan con más frecuencia en los equipos.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formas de dígito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668417"
---
# <a name="digit-shapes"></a>Formas de dígito

El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos occidentales convencionales que se usan con más frecuencia en los equipos. Para evitar la ambigüedad en la asignación de nombres a estas formas, en este documento se usan los siguientes nombres del estándar Unicode.



| Nombre Unicode de los dígitos                                     | País o región donde se usa                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Dígitos europeos                                                | Europa, América y muchos otros países o regiones       |
| Dígitos de Arabic-Indic                                            | Países o regiones árabes (aunque muchos usan dígitos europeos) |
| Otros dígitos nacionales: dígitos índicos, dígitos tailandeses y similares | Varios países o regiones                                    |



 

Unicode proporciona puntos de código independientes para cada forma de dígito. Por lo tanto, para tener acceso a las formas de dígitos del idioma especial, la aplicación puede usar los códigos de caracteres Unicode pertinentes para los dígitos anteriores, U + 0030 a U + 0039. Estos códigos siempre se muestran con la forma adecuada, en función de la disponibilidad de la fuente.

Los códigos de caracteres Unicode U + 0030 a U + 0039 representan nominalmente los dígitos europeos del 0 al 9, pero se puede modificar su forma de dígito. Las API de texto GDI y DirectWrite proporcionan mecanismos para que las aplicaciones controlen este comportamiento. (Vea, por ejemplo, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) o [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution)). El comportamiento en algunos controles de Shell y marcos de la interfaz de usuario puede responder a la configuración regional del usuario para la sustitución de dígitos. la configuración [regional \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE se puede usar para obtener la configuración de sustitución de dígitos predeterminada para diferentes configuraciones regionales o la configuración de escritorio del usuario actual para la sustitución de dígitos.

## <a name="native-digits"></a>Dígitos nativos

Los dígitos nativos son las formas de dígitos que elige el usuario en la hoja de propiedades **número** de la parte configuración regional y de idioma del panel de control. Para buscar la presentación de dígitos preferida por el usuario, la aplicación usa la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ SNATIVEDIGITS de configuración regional](locale-snative-constants.md) que representa la información de configuración regional.

> [!Note]  
> Normalmente, los códigos de dígitos Unicode se generan en rutinas del sistema operativo en tiempo de ejecución. Por lo tanto, los sistemas operativos en tiempo de ejecución comunes deben actualizarse para que la aplicación inspeccione de forma adecuada la [configuración regional \_ SNATIVEDIGITS](locale-snative-constants.md) .

 

## <a name="digit-substitution"></a>Sustitución de dígitos

La aplicación puede utilizar la sustitución de dígitos para indicar al sistema operativo cómo imprimir dígitos U + 0030 a U + 0039. La constante [ \_ IDIGITSUBSTITUTION de configuración regional](locale-idigitsubstitution.md) controla esta operación.

## <a name="digit-shaping-for-a-single-function"></a>Forma de dígitos para una sola función

Las funciones de [ \_ resultados](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)y GCP tienen marcas que rigen la sustitución de códigos Unicode U + 0030 a u + 0039 mientras dure la llamada a la función. Estas marcas invalidan la configuración regional en el panel de control, pero no restablecen la configuración. Además, no invalidan los códigos Unicode NADS y nodos. Están disponibles las marcas siguientes.



| Marcas                 | Dígitos usados                      | Se usa en                   |
|-----------------------|----------------------------------|---------------------------|
| ETO \_ NUMERICSLATIN    | Dígitos europeos                  | **ExtTextOut**            |
| ETO \_ NUMERICSLOCAL    | Dígitos adecuados para la configuración regional | **ExtTextOut**            |
| \_NUMERICSLATIN GCP    | Dígitos europeos                  | **GetCharacterPlacement** |
| \_NUMERICSLOCAL GCP    | Dígitos adecuados para la configuración regional | **GetCharacterPlacement** |
| GCPCLASS \_ LATINNUMBER | Dígitos europeos                  | **resultados de GCP \_**          |
| GCPCLASS \_ LOCALNUMBER | Dígitos adecuados para la configuración regional | **resultados de GCP \_**          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
