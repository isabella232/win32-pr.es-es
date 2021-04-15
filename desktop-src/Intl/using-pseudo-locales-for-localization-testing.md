---
description: En Windows Vista y versiones posteriores, puede usar pseudo-configuraciones regionales para probar la localizabilidad de las aplicaciones. En este tema se incluyen procedimientos para usar pseudo-codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Usar pseudo-configuraciones regionales para pruebas de localizabilidad
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688693"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a>Usar pseudo-configuraciones regionales para pruebas de localizabilidad

Las [pseudo configuraciones regionales](pseudo-locales.md) están integradas en Windows Vista y versiones posteriores, por lo que puede tener acceso a ellas a través de las API de compatibilidad con el idioma nacional (NLS). Puede usar pseudo-configuraciones regionales para probar la [localizabilidad](/windows/uwp/design/globalizing/globalizing-portal) de las aplicaciones. En este tema se incluyen procedimientos para usar pseudo-codes.

> [!NOTE]
> Una tarea que necesita una consideración especial en el momento en que se enumeran las configuraciones regionales, ya sea en el código o en la parte configuración regional y de idioma del panel de control. Más adelante en este tema.

Los nombres de las pseudo-configuraciones regionales son "QPS-PLOC", "QPS-Ploca" y "QPS-plocm". A partir de Windows 10, también está disponible la pseudo configuración regional "QPS-latn-x-SH".

## <a name="retrieve-information-about-pseudo-locales"></a>Recuperación de información acerca de las pseudo-configuraciones regionales

Puede usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) para recuperar información sobre una pseudo-configuración regional. Pase a la función el nombre de la pseudo-configuración regional concreta (vea la lista de nombres anteriores). Por ejemplo, "QPS-plocm" para la pseudo-configuración regional reflejada.

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a>Uso de LocaleNameToLCID con pseudo-configuraciones regionales

Puede llamar a la función de asignación NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con el nombre de una pseudo-configuración regional.

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a>Habilitar las pseudo-configuraciones regionales para la enumeración

En la aplicación, puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) para enumerar las configuraciones regionales que reconoce el sistema. La parte de las opciones de configuración regional y de idioma del panel de control también llama a **EnumSystemLocalesEx** para generar la lista de configuraciones regionales que muestra. Sin embargo, de forma predeterminada, el sistema no reconoce las cuatro pseudo configuraciones regionales mencionadas anteriormente, por lo que **EnumSystemLocalesEx** no las devolverá. En el caso de los sistemas desde Windows vista hasta la versión 1709 de Windows 10, la solución es habilitar las pseudo-configuraciones regionales agregando claves al registro de Windows.

Las modificaciones se realizan en la clave de \_ \_ \\ NLS del control System de la máquina local HKEY \\ \\ \\ para los idiomas instalados en el sistema operativo. Puede establecer esta configuración para habilitar las pseudo configuraciones regionales. Cada clave que se muestra a continuación es el LCID hexadecimal correspondiente a la configuración regional que se está habilitando. Cada valor es de tipo String (REG \_ SZ).

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

En Windows 10, versión 1803, la edición del registro de Windows como esta no tiene ningún efecto. Pero puede seguir llamando a las API NLS sin enumeración con los nombres de las pseudo-configuraciones regionales (vea los ejemplos de código anteriores) para rellenar la interfaz de usuario (UI).

## <a name="related-topics"></a>Temas relacionados

* [Uso de la compatibilidad con National Language](using-national-language-support.md)
* [Pseudo-configuraciones regionales](pseudo-locales.md)
* [EnumSystemLocalesEx](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [GetLocaleInfoEx](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [LocaleNameToLCID](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
