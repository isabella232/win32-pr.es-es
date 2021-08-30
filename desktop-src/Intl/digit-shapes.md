---
description: El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos del oeste convencionales que se usan con más frecuencia en los equipos.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formas de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fa63f26cceb3c3e819e754461330bb190a260013211c4a37e05eb0c816164d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083025"
---
# <a name="digit-shapes"></a>Formas de dígitos

El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos del oeste convencionales que se usan con más frecuencia en los equipos. Para evitar ambigüedades en la asignación de nombres a estas formas, en este documento se usan los siguientes nombres del estándar Unicode.



| Nombre Unicode de los dígitos                                     | País o región donde se usa                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Dígitos europeos                                                | Europa, América y muchos otros países o regiones       |
| Arabic-Indic dígitos                                            | Países o regiones árabes (aunque muchos usan dígitos europeos) |
| Otros dígitos nacionales: dígitos nódicos, dígitos tailandeses y otros tipos | Varios países o regiones                                    |



 

Unicode proporciona puntos de código independientes para cada forma de dígito. Por lo tanto, para acceder a formas de dígitos de idioma especiales, la aplicación puede usar los códigos de caracteres Unicode pertinentes para los dígitos anteriores, de U+0030 a U+0039. Estos códigos siempre se muestran con la forma adecuada, sujeto a disponibilidad de fuentes.

Los códigos de caracteres Unicode U+0030 a U+0039 representan nominalmente los dígitos europeos del 0 al 9, pero su forma de dígito se puede modificar. Las API de texto DirectWrite GDI y de texto proporcionan mecanismos para que las aplicaciones controle este comportamiento. (Vea, por ejemplo, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) o [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution)). El comportamiento en algunos controles de shell y marcos de interfaz de usuario puede responder a la configuración regional del usuario para la sustitución de dígitos. [LOCALE \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE se puede usar para obtener la configuración predeterminada de sustitución de dígitos para diferentes configuraciones regionales o la configuración de escritorio del usuario actual para la sustitución de dígitos.

## <a name="native-digits"></a>Dígitos nativos

Los dígitos nativos son las  formas de dígito elegidas por el usuario en la hoja de propiedades Número en la parte de opciones regionales y de idioma de la Panel de control. Para buscar la presentación de dígitos preferida por el usuario, la aplicación usa la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ LOCALE SNATIVEDIGITS](locale-snative-constants.md) que representa la información de configuración regional.

> [!Note]  
> Normalmente, los códigos de dígitos Unicode se generan en rutinas del sistema operativo en tiempo de ejecución. Por lo tanto, los sistemas operativos common runtime deben actualizarse para que la aplicación inspeccione [LOCALE \_ SNATIVEDIGITS](locale-snative-constants.md) adecuadamente.

 

## <a name="digit-substitution"></a>Sustitución de dígitos

La aplicación puede usar la sustitución de dígitos para decir al sistema operativo cómo imprimir los dígitos U+0030 a U+0039. La [constante \_ LOCALE IDIGITSUBSTITUTION](locale-idigitsubstitution.md) controla esta operación.

## <a name="digit-shaping-for-a-single-function"></a>Modelado de dígitos para una sola función

Las [funciones ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)y [GCP \_ RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) tienen marcas que rigen la sustitución de códigos Unicode U+0030 a U+0039 durante la llamada de función. Estas marcas invalidan la configuración regional en el Panel de control, pero no restablecen la configuración. Además, no invalidan los códigos Unicode NADS y NODS. Las marcas siguientes están disponibles.



| Marcas                 | Dígitos usados                      | Se usa en                   |
|-----------------------|----------------------------------|---------------------------|
| ETO \_ NUMERICSLATIN    | Dígitos europeos                  | **ExtTextOut**            |
| ETO \_ NUMERICSLOCAL    | Dígitos adecuados para la configuración regional | **ExtTextOut**            |
| GCP \_ NUMERICSLATIN    | Dígitos europeos                  | **GetCharacterPlacement** |
| GCP \_ NUMERICSLOCAL    | Dígitos adecuados para la configuración regional | **GetCharacterPlacement** |
| GCPCLASS \_ LATINNUMBER | Dígitos europeos                  | **Resultados de \_ GCP**          |
| GCPCLASS \_ LOCALNUMBER | Dígitos adecuados para la configuración regional | **Resultados de \_ GCP**          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
