---
description: En Windows Vista y versiones posteriores, puede usar pseudo-configuraciones regionales para probar la localizabilidad de las aplicaciones. En este tema se incluyen procedimientos para usar pseudocódigos.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Uso de pseudo-configuraciones regionales para pruebas de localizabilidad
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: 72d84cbf324823a814c9412580b033792b0d1c8a45630bf2f4cb26dd8b2a1acf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631725"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Uso de pseudo-configuraciones regionales para pruebas de localizabilidad

[Las pseudo-configuraciones](pseudo-locales.md) regionales están integradas para Windows Vista y versiones posteriores, de modo que pueda acceder a ellas a través de las API de compatibilidad con idiomas nacionales (NLS). Puede usar pseudo-configuraciones regionales para probar la [localizabilidad](/windows/uwp/design/globalizing/globalizing-portal) de las aplicaciones. En este tema se incluyen procedimientos para usar pseudocódigos.

> [!NOTE]
> Una tarea que necesita una consideración especial en lo que respecta a las pseudo-configuraciones regionales es enumerarlos; ya sea en el código o en la parte regional y de opciones de idioma de la Panel de control. Más información al respecto más adelante en este tema.

Los nombres de las pseudo-configuraciones regionales son "qps-ploc", "qps-trucca" y "qps-truccm". A Windows 10, también está disponible la pseudo-configuración regional "qps-Latn-x-sh".

## <a name="retrieve-information-about-pseudo-locales"></a>Recuperación de información sobre pseudo-configuraciones regionales

Puede usar [**GetLocaleInfoEx para**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) recuperar información sobre una pseudo-configuración regional. Pase a la función el nombre de la pseudo-configuración regional concreta (consulte la lista de nombres anterior). Por ejemplo, "qps-truccm" para la pseudo-configuración regional reflejada.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Uso de LocaleNameToLCID con pseudo-configuraciones regionales

Puede llamar a la función de asignación NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con el nombre de una pseudo-configuración regional.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Habilitación de pseudo-configuraciones regionales para la enumeración

En la aplicación, puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) para enumerar las configuraciones regionales que el sistema reconoce. La parte de opciones regionales y de idioma del Panel de control también llama **a EnumSystemLocalesEx para** compilar la lista de configuraciones regionales que muestra. Sin embargo, de forma predeterminada, el sistema no reconoce las cuatro pseudo-configuraciones regionales enumeradas anteriormente, por lo que **EnumSystemLocalesEx** no las devolverá. Para los sistemas de Windows Vista hasta Windows 10, versión 1709, la solución es habilitar pseudo-configuraciones regionales mediante la adición de claves al Windows Registry.

Las modificaciones se realizan en la clave HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet Control Nls para los \\ \\ idiomas instalados en el sistema operativo. Puede realizar esta configuración para habilitar las pseudo-configuraciones regionales. Cada clave que se muestra a continuación es el LCID hexadecimal correspondiente a la pseudo-configuración regional que se está habilitando. Cada valor es de tipo cadena (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

Por Windows 10, versión 1803, la edición de Windows Registry como esta no tiene ningún efecto. Pero todavía puede llamar a las API de NLS que no se enumeran con los nombres de las pseudo-configuraciones regionales (consulte los ejemplos de código anteriores) para rellenar la interfaz de usuario (UI).

## <a name="related-topics"></a>Temas relacionados

* [Uso de la compatibilidad con idiomas nacionales](using-national-language-support.md)
* [Pseudo-Configuraciones regionales](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
