---
description: En este tema se describe cómo Windows Search admite varios idiomas.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Idiomas admitidos por búsqueda de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808977"
---
# <a name="languages-supported-by-windows-search"></a>Idiomas admitidos por búsqueda de Windows

En este tema se describe cómo Windows Search admite varios idiomas.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Tokenización, Wordbreakers y recursos de idioma

Windows Search es independiente del lenguaje, pero la precisión de la búsqueda en todos los idiomas puede variar debido a la manera en que wordbreakers el texto de tokens. Wordbreakers implemente varias reglas de tokenización para idiomas e divida el texto en tokens o palabras individuales, que se van a indexar o buscar.

El lenguaje del texto indexado y la cadena de consulta se dividen en tokens. Dado que las reglas de tokenización varían según el lenguaje, hay wordbreakers independientes para cada idioma o familia de idiomas. Si hay una discrepancia entre el lenguaje de consulta y el lenguaje indizado, los resultados pueden ser imprevisibles.

Windows Search incluye un conjunto bien definido de wordbreakers. Los componentes del separador clásico y lingüísticos son compatibles con Windows Vista y versiones posteriores. Si no se puede determinar el idioma de un documento, Windows Search intenta detectar el idioma para identificar el separador más apropiado. Windows Search intenta detectar el idioma mediante una llamada a la función [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) para determinar el primer idioma de la interfaz de usuario múltiple (MUI) (que suele ser el idioma de la interfaz de usuario del sistema, a menos que se instalen paquetes de idioma MUI). Si la llamada se realiza correctamente, se usa el separador del primer idioma de MUI. Si se produce un error en la llamada a **GetSystemPreferredUILanguages** , Windows Search recupera la configuración regional del sistema mediante una llamada a la función [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) y usa el separador asociado a esa configuración regional.

Si no hay ningún separador instalado para un idioma, Windows Search interrumpe el espacio en blanco mediante el separador **neutro** .

Puede quitar un idioma a través del registro, como se muestra en el ejemplo siguiente.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            ContentIndex
               Language
                  Dutch_Dutch
                     (Default)
                     Locale
                     NoiseFile
                     StemmerClass = CLSID
                     WBreakerClass = CLSID
```

> [!TIP]
> Si realiza cambios en el registro, reinicie Windows Search.

 

Cuando Windows Search requiere un nuevo separador, se lee el identificador de clase (CLSID) y se almacena en caché el separador con instancias.

Puede crear un separador personalizado para un idioma implementando la interfaz [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) . Windows Search llama a los métodos **IWordBreaker** cuando compila índices de contenido y ejecuta consultas.

La información de configuración regional del contenido indizado se recupera del origen del contenido. Si el implementador de origen no conoce la configuración regional del contenido indizado, debe establecer la configuración regional en [**\_ independiente de la configuración regional**](../intl/locale-neutral.md).

Por ejemplo, si implementa un controlador de filtro (una implementación de la interfaz [**IFilter**](https://www.bing.com/search?q=**IFilter**) ), un controlador de propiedad o un controlador de protocolo, debe establecer la configuración regional del contenido indizado en [**\_ independiente**](../intl/locale-neutral.md) de la configuración regional a menos que tenga información de configuración regional específica y esté seguro de su precisión.

> [!TIP]
> Si una consulta de índice se basa en la entrada del usuario, la configuración regional debe coincidir con el idioma en el que está escribiendo el usuario. Puede determinar esta configuración regional mediante una llamada a la función [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) .

 

## <a name="languages-supported-by-wordbreakers"></a>Idiomas admitidos por Wordbreakers

Windows Search incluye wordbreakers para admitir los siguientes lenguajes.



| Clave del Registro             | Idioma (subidioma)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_Saudiarabia Árabe**  | Árabe (neutro)                                  | 0x0001 |
| **\_Valor predeterminado de bengalí**     | Bangla (neutro)                                  | 0x0045 |
| **\_Valor predeterminado de búlgaro**   | Búlgaro (Bulgaria)                              | 0x0402 |
| **Catalán ( \_ valor predeterminado)**     | Catalán (España)                                 | 0x0403 |
| **Chino \_ Hong Kong**    | Chino (Hong Kong ZAE, RPC)                      | 0x0C04 |
| **Chino \_ simplificado**  | Chino (simplificado)                              | 0x0804 |
| **Chino \_ tradicional** | Chino (tradicional)                             | 0x0404 |
| **\_Valor predeterminado de croata**    | Croata (Croacia)                                | 0x041A |
| **\_Valor predeterminado Checo**       | Checo (República Checa)                            | 0x0405 |
| **Danés \_ predeterminado**      | Danés (Dinamarca)                                  | 0x0406 |
| **\_Holandés Holandés**         | Neerlandés (Países Bajos)                               | 0x0413 |
| **Inglés ( \_ Reino Unido)**          | Inglés (Reino Unido)                          | 0x0809 |
| **Inglés de \_ EE. UU.**          | Spanish (Traditional Sort) - Spain                           | 0x0409 |
| **Finés, \_ valor predeterminado**     | Finés (Finlandia)                                 | 0x040B |
| **Francés \_ Francés**       | Francés (Francia)                                   | 0x040C |
| **Alemán \_ alemán**       | Alemán (Alemania)                                  | 0x0407 |
| **Griego \_ predeterminado**       | Griego (Grecia)                                    | 0x0408 |
| **\_Valor predeterminado de Gujarati**    | Gujarati (India)                                  | 0x0447 |
| **Hebreo \_ predeterminado**      | Hebreo (neutro)                                  | 0x000D |
| **\_Valor predeterminado Hindi**       | Hindi (India)                                     | 0x0439 |
| **Húngaro \_ predeterminado**   | Húngaro (Hungría)                               | 0x040E |
| **Islandés \_ predeterminado**   | Islandés (Islandia)                               | 0x040F |
| **\_Valor predeterminado de indonesio**  | Indonesio (Indonesia)                            | 0x0421 |
| **Italiano \_ Italiano**     | Italiano (Italia)                                   | 0x0410 |
| **Japonés \_ predeterminado**    | Japonés (Japón)                                  | 0x0411 |
| **\_Valor predeterminado de Kannada**     | Canarés (India)                                   | 0x044B |
| **Coreano \_ predeterminado**      | Coreano (Corea)                                    | 0x0412 |
| **\_Valor predeterminado de letón**     | Letón (Letonia)                                  | 0x0426 |
| **Lituano \_ predeterminado**  | Lituano (Lituano)                           | 0x0427 |
| **\_Malasia Malayo**      | Malayo (Malasia)                                  | 0x043E |
| **\_Valor predeterminado de Malayalam**   | Malayalam (neutro)                               | 0x004C |
| **\_Valor predeterminado de Marathi**     | Maratí (India)                                   | 0x044E |
| **Noruego \_ Bokmal**    | Noruego (Bokmål, Noruega)                        | 0x0414 |
| **Polaco \_ predeterminado**      | Polaco (Polonia)                                   | 0x0415 |
| **Portugués de \_ Portugal** | Portugués (Portugal)                             | 0x0816 |
| **Portugués de \_ Brasil**   | Portugués (Brasil)                               | 0x0416 |
| **Predeterminado de punjabí \_**     | Punjabí (India)                                   | 0x0446 |
| **\_Valor predeterminado de rumano**    | Rumano (Rumanía)                                | 0x0418 |
| **\_Valor predeterminado Ruso**     | Ruso (neutro)                                 | 0x0019 |
| **Serbio ( \_ cirílico)**    | Serbio (Serbia y Montenegro, ex, cirílico) | 0x0C1A |
| **Serbio \_ latín**       | Serbio (Serbia y Montenegro, ex, latín)    | 0x081A |
| **\_Valor predeterminado de eslovaco**      | Eslovaco (Eslovaquia)                                 | 0x041B |
| **\_Valor predeterminado de esloveno**   | Esloveno (Eslovenia)                              | 0x0424 |
| **Español \_ moderno**      | Español (España, alfabetización moderno)                      | 0x0C0A |
| **Sueco \_ predeterminado**     | Sueco (Suecia)                                  | 0x041D |
| **\_Valor predeterminado de Tamil**       | Tamil (India)                                     | 0x0449 |
| **\_Valor predeterminado de Telugu**      | Telugu (India)                                    | 0x044A |
| **\_Valor predeterminado tailandés**        | Tailandés (Tailandia)                                   | 0x041E |
| **Turco \_ predeterminado**     | Turco (Turquía)                                  | 0x041F |
| **\_Valor predeterminado de ucraniano**   | Ucraniano (Ucrania)                               | 0x0422 |
| **Predeterminado de Urdu \_**        | Urdú (Pakistán)                                   | 0x0420 |
| **\_Valor predeterminado vietnamita**  | Vietnamita (Vietnam)                              | 0x042A |



 

> [!Note]  
> Los LCID de algunos idiomas de la tabla se generan mediante el identificador de idioma, el identificador de subidioma y el identificador de ordenación.

 

Para obtener más información sobre los lenguajes y los identificadores asociados, vea [Language Identifier (constantes y cadenas](../intl/language-identifier-constants-and-strings.md)).

> [!Note]  
> No hay ninguna garantía de que todas estas claves del registro de idioma estén presentes en una máquina determinada. El separador de cualquier idioma determinado se puede instalar o no en el equipo en función de la configuración del usuario.

 

A **partir de Windows 8.1**, la manera preferida de usar wordbreakers es a través de la [**clase WORDSSEGMENTER**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)de la API de WinRT.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo implementar y usar separadores de palabras personalizados y lematizadores para idiomas y configuraciones regionales adicionales, consulte [extensión de recursos de idioma en Windows Search](extending-language-resources-in-windows-search.md).
-   Si necesita identificar el idioma de un fragmento de texto, puede usar la detección automática de idioma (LAD), que está disponible en Windows 7 y versiones posteriores. Para obtener más información, vea [servicios lingüísticos extendidos](../intl/extended-linguistic-services.md) (Els).
-   Para obtener información sobre la administración, la consulta y la extensión del índice, consulte la [Guía del desarrollador de Windows Search](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
