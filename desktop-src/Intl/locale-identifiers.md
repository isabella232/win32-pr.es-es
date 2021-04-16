---
description: Cada configuración regional tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de ordenación.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificadores de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686496"
---
# <a name="locale-identifiers"></a>Identificadores de configuración regional

Cada [configuración regional](locales-and-languages.md) tiene un identificador único, un valor de 32 bits que consta de un [identificador de idioma](language-identifiers.md) y un identificador de [criterio de ordenación](sort-order-identifiers.md). El identificador de configuración regional es una abreviatura numérica internacional estándar y tiene los componentes necesarios para identificar de forma única una de las configuraciones regionales definidas por el sistema operativo instaladas. NLS es compatible con los identificadores de configuración regional predefinidos y los identificadores personalizados.

> [!Note]  
> Los nombres de configuración regional se pueden usar con las funciones introducidas en Windows Vista que toman un [nombre de configuración regional](locale-names.md) como parámetro, en lugar de un identificador de configuración regional. Para obtener más información, consulte [llamar a las funciones de "nombre de la configuración regional"](calling-the--locale-name--functions.md). Siempre se prefiere el uso de nombres de configuración regional en lugar de los identificadores de configuración regional.

 

En la ilustración siguiente se muestra el formato de los bits en un identificador de configuración regional.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Identificadores de configuración regional predefinidos

Los identificadores de configuración regional predefinidos que admite NLS se definen en la referencia de la [API de compatibilidad con el idioma nacional (NLS)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

NLS usa las siguientes constantes de información de configuración regional para representar los identificadores de configuración regional.

-   [Configuración \_ regional SLANGUAGE](locale-slanguage.md) o [configuración regional \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [configuración regional \_ SNAME](locale-sname.md)
-   [configuración regional \_ SSCRIPTS](locale-sscripts.md)
-   [configuración regional \_ IDEFAULTANSICODEPAGE](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Identificadores de configuración regional personalizados

**Windows Vista:** NLS es compatible con los identificadores de configuración regional personalizados que representan las siguientes constantes de información de configuración regional.

-   [CONFIGURACIÓN \_ predeterminada personalizada \_](locale-custom-constants.md)
-   [CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_](locale-custom-constants.md)
-   [configuración regional \_ personalizada no \_ especificada](locale-custom-constants.md)

## <a name="building-a-locale"></a>Creación de una configuración regional

Puede usar la utilidad de configuración regional que proporciona NLS para compilar configuraciones regionales. Para obtener más información, vea [generador de configuración regional de Microsoft](https://www.microsoft.com/download/details.aspx?id=41158).

La aplicación puede construir un identificador de configuración regional mediante la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) . También puede usar uno de los identificadores predeterminados correspondientes a las constantes que se enumeran a continuación.

-   [configuración regional \_ INvariable](locale-invariant.md)
-   [configuración \_ predeterminada del sistema local \_](locale-system-default.md)
-   [\_valor predeterminado del usuario de configuración regional \_](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Recuperación de los identificadores de configuración regional

Una aplicación puede recuperar los identificadores de configuración regional actuales mediante las funciones [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) y [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) . Cada subproceso puede establecer y recuperar su propia configuración regional con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) y [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Identificadores de idioma](language-identifiers.md)
</dt> <dt>

[Nombres de configuración regional](locale-names.md)
</dt> <dt>

[Identificadores de criterio de ordenación](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
