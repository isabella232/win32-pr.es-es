---
description: Cada configuración regional tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de ordenación.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificadores de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063074"
---
# <a name="locale-identifiers"></a>Identificadores de configuración regional

Cada [configuración regional](locales-and-languages.md) tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de [ordenación](sort-order-identifiers.md). [](language-identifiers.md) El identificador de configuración regional es una abreviatura numérica internacional estándar y tiene los componentes necesarios para identificar de forma única una de las configuraciones regionales definidas por el sistema operativo instalado. NLS admite identificadores de configuración regional predefinidos e identificadores personalizados.

> [!Note]  
> Los nombres de configuración regional se pueden usar con funciones introducidas en Windows Vista que toman un nombre de configuración [regional](locale-names.md) como parámetro, en lugar de un identificador de configuración regional. Para obtener más información, vea [Llamar a las funciones "Nombre de configuración regional".](calling-the--locale-name--functions.md) Siempre es preferible usar nombres de configuración regional en lugar de identificadores de configuración regional.

 

En la ilustración siguiente se muestra el formato de los bits en un identificador de configuración regional.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Identificadores de configuración regional predefinidos

Los identificadores de configuración regional predefinidos admitidos por NLS se definen en la referencia de la API de compatibilidad con el lenguaje [nacional (NLS).](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c)

NLS usa las siguientes constantes de información de configuración regional para representar los identificadores de configuración regional.

-   [CONFIGURACIÓN REGIONAL \_ SLANGUAGE o](locale-slanguage.md) [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [LOCALE \_ SNAME](locale-sname.md)
-   [SSCRIPT \_ DE CONFIGURACIÓN REGIONAL](locale-sscripts.md)
-   [CONFIGURACIÓN REGIONAL \_ IDEFAULTANSICODEPAGE](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Identificadores de configuración regional personalizados

**Windows Vista:** NLS admite los identificadores de configuración regional personalizados representados por las siguientes constantes de información de configuración regional.

-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DE LA INTERFAZ DE USUARIO \_ \_ PERSONALIZADA](locale-custom-constants.md)
-   [CONFIGURACIÓN REGIONAL \_ PERSONALIZADA \_ SIN ESPECIFICAR](locale-custom-constants.md)

## <a name="building-a-locale"></a>Creación de una configuración regional

Puede usar la utilidad Generador de configuración regional proporcionada por NLS para compilar configuraciones regionales. Para obtener más información, vea [Generador de configuración regional de Microsoft](https://www.microsoft.com/download/details.aspx?id=41158).

La aplicación puede construir un identificador de configuración regional mediante la [**macro MAKELCID.**](/windows/desktop/api/Winnt/nf-winnt-makelcid) Como alternativa, puede usar uno de los identificadores predeterminados correspondientes a las constantes enumeradas a continuación.

-   [CONFIGURACIÓN REGIONAL \_ INVARIABLE](locale-invariant.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ SISTEMA](locale-system-default.md)
-   [CONFIGURACIÓN REGIONAL \_ PREDETERMINADA DEL \_ USUARIO](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Recuperación de identificadores de configuración regional

Una aplicación puede recuperar los identificadores de configuración regional actuales mediante las funciones [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) y [**GetUserDefaultLCID.**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) Cada subproceso puede establecer y recuperar su propia configuración regional con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) y [**GetThreadLocale.**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)

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

 

 
