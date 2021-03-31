---
title: Llamar a WDS desde páginas web
description: Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante el objeto auxiliar de explorador (BHO) y Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "104077424"
---
# <a name="calling-wds-from-web-pages"></a>Llamar a WDS desde páginas web

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante el objeto auxiliar de explorador (BHO) y Windows Internet Explorer. Puede ver cómo funciona esto en la Página Web de MSN. Encima del cuadro de búsqueda en https://www.msn.com hay varios tipos de búsqueda: Web, News, images, Desktop, Encarta y local. Si hace clic en escritorio, los parámetros de búsqueda se pasan a la búsqueda de escritorio de Windows, que busca en el catálogo y muestra los resultados en la interfaz de usuario de WDS. Para que los usuarios puedan iniciar una búsqueda en el escritorio desde las páginas web, el WDSBHO debe estar instalado y habilitado en sus sistemas, las páginas web deben estar registradas con WDS como una dirección URL permitida y debe crear un vínculo para pasar la consulta User-enetered a WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Habilitar el objeto de ayuda del explorador de WDS

El BHO se instala y se habilita en Internet Explorer de forma predeterminada al instalar WDS, pero puede comprobar fácilmente que no se ha deshabilitado o desinstalado. En el sistema de un usuario, abra Internet Explorer, seleccione **Opciones de Internet** en el menú **herramientas** , haga clic en la pestaña **programas** y, a continuación, haga clic en **Administrar complementos**. En la lista de complementos, busque la clase dsWebAllowBHO y asegúrese de que está habilitada. Cuando se deshabilita el BHO, WDS seguirá funcionando con normalidad; sin embargo, no podrá buscar en el escritorio desde una página web.

Las dos opciones siguientes para permitir una búsqueda en el escritorio ejecutarán la búsqueda localmente con la aplicación de búsqueda registrada.

## <a name="registering-web-page-urls"></a>Registro de direcciones URL de páginas web

El registro incluye una lista de direcciones URL de dominio "permitidas" desde las que se puede llamar a WDS. Para incluir las páginas web, debe mostrar las direcciones URL de dominio como REG \_ SZ en el registro como se indica a continuación:

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **permitido**\\*<number>* = <domainURL>

Donde **<number>** se numera secuencialmente, y **<domainURL>** es la dirección URL de la Página Web de la que desea permitir búsquedas de WDS. Esta cadena de dirección URL puede incluir el asterisco comodín \* al principio o al final de la dirección URL. Por ejemplo, si la cadena es " \* . mydomain.com", puede iniciar una búsqueda de WDS desde https://www.mydomain.com y https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Habilitación de la búsqueda en el escritorio por dirección URL

Otra opción que no requiere acceso al registro es usar la siguiente dirección URL en las páginas web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

donde **query** es la cadena con codificación URL en la que el usuario realiza la búsqueda, incluidos los términos de [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md) .

 

 




