---
description: En este tema se describe cómo Windows Search admite varios idiomas.
ms.assetid: a800d2ac-3aee-4e74-a29a-a70355138ebc
title: Idiomas admitidos por Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350a8861a5817a8ac5710214ccd35c780f2c9dd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363298"
---
# <a name="languages-supported-by-windows-search"></a>Idiomas admitidos por Windows Search

En este tema se describe cómo Windows Search admite varios idiomas.

## <a name="tokenization-wordbreakers-and-language-resources"></a>Tokenización, wordbreakers y recursos de lenguaje

Windows La búsqueda es independiente del idioma, pero la precisión de la búsqueda entre idiomas puede variar debido a la forma en que los usuarios de la función de palabras tokenizan texto. Los buscadores de palabras implementan varias reglas de tokenización para los idiomas y separan el texto en tokens individuales, o palabras, que se indexan o buscan.

Tanto el idioma del texto indexado como la cadena de consulta se divide en tokens. Dado que las reglas de tokenización varían según el idioma, hay separadores de palabras para cada idioma o familia de idiomas. Si hay una discrepancia entre el lenguaje de consulta y el idioma indexado, los resultados pueden ser impredecibles.

Windows La búsqueda se distribuye con un conjunto bien definido de desgarradores de palabras. Los componentes clásicos del cortador de palabras y lematizadores se admiten en Windows Vista y versiones posteriores. Si no se puede determinar el idioma de un documento, Windows Search intenta detectar el idioma para identificar el que se encuentra más adecuado. Windows La búsqueda intenta detectar el idioma mediante una llamada a la función [**GetSystemPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getsystempreferreduilanguages) para determinar el primer idioma de Multiple Interfaz de usuario (INTERFAZ DE USUARIO) (que suele ser el idioma de la interfaz de usuario del sistema a menos que estén instalados los paquetes de idioma DE ACUERDO). Si esa llamada se realiza correctamente, se usa el cortador de palabras para el primer idioma DE LAN. Si se produce un error en la llamada a **GetSystemPreferredUILanguages,** Windows Search recupera la configuración regional del sistema mediante una llamada a la función [**GetSystemDefaultLCID**](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlcid) y usa el corta palabras asociado a esa configuración regional.

Si no hay ningún cortador de palabras instalado para un idioma, Windows búsqueda se interrumpe en el espacio en blanco mediante el **corta** palabras neutro.

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
> Si realiza cambios en el Registro, reinicie Windows Buscar.

 

Cuando Windows search requiere un nuevo corta palabras, se lee el identificador de clase (CLSID) y se almacena en caché el corta palabras con instancias.

Puede crear un corta palabras personalizado para un lenguaje mediante la implementación de la [**interfaz IWordBreaker.**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) Windows A continuación, search llama **a los métodos IWordBreaker** cuando compila índices de contenido y ejecuta consultas.

La información de configuración regional del contenido indexado se recupera del origen del contenido. Si el implementador de origen no conoce la configuración regional del contenido indexado, debe establecer la configuración regional en [**LOCALE \_ NEUTRAL.**](../intl/locale-neutral.md)

Por ejemplo, si implementa un controlador de filtro (una implementación de la interfaz [**IFilter),**](https://www.bing.com/search?q=**IFilter**) el controlador de propiedades o el controlador de protocolo, debe establecer la configuración regional del contenido indexado en [**LOCALE \_ NEUTRAL**](../intl/locale-neutral.md) a menos que tenga información de configuración regional específica y esté seguro de su precisión.

> [!TIP]
> Si una consulta de índice se basa en la entrada del usuario, la configuración regional debe coincidir con el idioma en el que el usuario escribe. Puede determinar esta configuración regional llamando a la [**función GetKeyboardLayout.**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)

 

## <a name="languages-supported-by-wordbreakers"></a>Idiomas admitidos por los wordbreakers

Windows La búsqueda incluye los buscadores de palabras para admitir los idiomas siguientes.



| Clave del Registro             | Language (sublanguage)                            | LCID   |
|--------------------------|---------------------------------------------------|--------|
| **\_Arabic ArabicArabia**  | Árabe (neutro)                                  | 0x0001 |
| **Predeterminado de \_ Bengali**     | Jadela (neutral)                                  | 0x0045 |
| **Predeterminado de \_ la omisión**   | Búlgaro (Bulgaria)                              | 0x0402 |
| **Default \_ de Catar**     | Catalán (España)                                 | 0x0403 |
| **Chino \_ HongKong**    | Chino (Hong Kong ZAE, RPC)                      | 0x0C04 |
| **Chino \_ simplificado**  | Chino (simplificado)                              | 0x0804 |
| **Chino \_ tradicional** | Chino (tradicional)                             | 0x0404 |
| **Valor predeterminado \_ deenseense**    | Croata (Croacia)                                | 0x041A |
| **Valor \_ predeterminado checo**       | Checo (República Checa)                            | 0x0405 |
| **Valor \_ predeterminado danés**      | Danés (Dinamarca)                                  | 0x0406 |
| **Neerlandés \_ neerlandés**         | Neerlandés (Países Bajos)                               | 0x0413 |
| **Inglés \_ (Reino Unido)**          | Inglés (Reino Unido)                          | 0x0809 |
| **Inglés \_ de EE. UU.**          | Spanish (Traditional Sort) - Spain                           | 0x0409 |
| **Valor predeterminado \_ finés**     | Finés (Finlandia)                                 | 0x040B |
| **Francés \_**       | Francés (Francia)                                   | 0x040C |
| **Alemán \_ alemán**       | Alemán (Alemania)                                  | 0x0407 |
| **Valor predeterminado \_ griego**       | Griego (Grecia)                                    | 0x0408 |
| **Valor predeterminado de Gujarati \_**    | Gujarati (India)                                  | 0x0447 |
| **Valor \_ predeterminado hebreo**      | Hebreo (neutro)                                  | 0x000D |
| **Valor predeterminado de \_ Hindi**       | Hindi (India)                                     | 0x0439 |
| **Valor \_ predeterminado húngaro**   | Húngaro (Hungría)                               | 0x040E |
| **Valor predeterminado \_ islandés**   | Islandés (Islandia)                               | 0x040F |
| **Predeterminado \_ indonesio**  | Indonesio (Indonesia)                            | 0x0421 |
| **Italiano \_**     | Italiano (Italia)                                   | 0x0410 |
| **Valor \_ predeterminado japonés**    | Japonés (Japón)                                  | 0x0411 |
| **Valor predeterminado de Kannada \_**     | Canarés (India)                                   | 0x044B |
| **Valor \_ predeterminado coreano**      | Coreano (Corea)                                    | 0x0412 |
| **Valor predeterminado de \_ Letón**     | Letón (Letonia)                                  | 0x0426 |
| **Valor predeterminado \_ lituano**  | Lituano (lituano)                           | 0x0427 |
| **Malaya \_**      | Malayo (Malasia)                                  | 0x043E |
| **Valor predeterminado de \_ Malayalam**   | Malayalam (neutro)                               | 0x004C |
| **Valor predeterminado de Marathi \_**     | Maratí (India)                                   | 0x044E |
| **Noruego \_ Bokmal**    | Noruego (Bokmål, Noruega)                        | 0x0414 |
| **Valor \_ predeterminado de Polaco**      | Polaco (Polonia)                                   | 0x0415 |
| **Portugués \_ de Portugal** | Portugués (Portugal)                             | 0x0816 |
| **Portugués \_ de Brasil**   | Portugués (Brasil)                               | 0x0416 |
| **Valor predeterminado de \_ Punjabi**     | Punjabí (India)                                   | 0x0446 |
| **Valor predeterminado \_ de Rulo**    | Rumano (Rumanía)                                | 0x0418 |
| **Valor \_ predeterminado de Ruso**     | Ruso (neutro)                                 | 0x0019 |
| **Cirílico serbio \_**    | Serbio (Serbia y Antigua, Cirílico) | 0x0C1A |
| **Latino \_ serbio**       | Serbio (Serbia y Fuenco, Antiguo, Latino)    | 0x081A |
| **Valor predeterminado \_ de omisión**      | Eslovaco (Eslovaquia)                                 | 0x041B |
| **Valor predeterminado de LaN \_**   | Esloveno (Eslovenia)                              | 0x0424 |
| **Español \_ moderno**      | Español (España, Ordenación moderna)                      | 0x0C0A |
| **Valor predeterminado \_ de sueco**     | Sueco (Suecia)                                  | 0x041D |
| **Valor predeterminado de \_ Tamil**       | Tamil (India)                                     | 0x0449 |
| **Valor predeterminado de Telugu \_**      | Telugu (India)                                    | 0x044A |
| **Valor \_ predeterminado tailandés**        | Tailandés (Tailandia)                                   | 0x041E |
| **Valor \_ predeterminado turco**     | Turco (Turquía)                                  | 0x041F |
| **Valor \_ predeterminado de 4000**   | Ucraniano (Ucrania)                               | 0x0422 |
| **Valor predeterminado de Urdu \_**        | Urdú (Pakistán)                                   | 0x0420 |
| **Valor \_ predeterminado de omisión**  | Vietnamita (Vietnam)                              | 0x042A |



 

> [!Note]  
> Los LCID para algunos idiomas de la tabla se generan mediante el identificador de idioma, el identificador de subidioma y el identificador de ordenación.

 

Para obtener más información sobre los idiomas y los identificadores asociados, vea Constantes y cadenas de [identificador de lenguaje.](../intl/language-identifier-constants-and-strings.md)

> [!Note]  
> No hay ninguna garantía de que todas estas claves del Registro de lenguaje estarán presentes en cualquier máquina determinada. El wordbreaker de cualquier idioma determinado puede o no instalarse en la máquina en función de la configuración del usuario.

 

**A partir Windows 8.1**, la manera preferida de usar los wordbreakers es a través de la clase [**WordsSegmenter**](/uwp/api/Windows.Data.Text.WordsSegmenter?view=winrt-19041)de la API de WinRT.

## <a name="additional-resources"></a>Recursos adicionales

-   Para obtener información sobre cómo implementar y usar separadores de palabras y lematizadores personalizados para idiomas y configuraciones regionales adicionales, vea Extender recursos de idioma [en Windows Search](extending-language-resources-in-windows-search.md).
-   Si necesita identificar el idioma de un fragmento de texto, puede usar la detección automática de idioma (LAD), que está disponible en Windows 7 y versiones posteriores. Para obtener más información, vea [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).
-   Para obtener información sobre cómo administrar, consultar y ampliar el índice, consulte la guía del desarrollador [Windows Search](-search-developers-guide-entry-page.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Search como plataforma de desarrollo](-search-3x-wds-development-ovr.md)
</dt> <dt>

[Uso de código administrado con datos de shell y Windows Search](-search-3x-wds-managed-code.md)
</dt> </dl>

 

 
