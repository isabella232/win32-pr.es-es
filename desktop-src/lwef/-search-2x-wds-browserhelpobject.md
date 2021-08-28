---
title: Llamada a WDS desde Páginas web
description: Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante browser Helper Object (BHO) y Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2be6be30889e8f759ee3cf7529250a5513ce58
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883706"
---
# <a name="calling-wds-from-web-pages"></a>Llamada a WDS desde Páginas web

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Puede llamar a Microsoft Windows Desktop Search (WDS) desde cualquier página web que cree o mantenga mediante browser Helper Object (BHO) y Windows Internet Explorer. Puede ver cómo funciona esto en la página web de MSN. Encima del cuadro de búsqueda de hay varios tipos https://www.msn.com de búsqueda: Web, Noticias, Imágenes, Escritorio, Encarta y Local. Si hace clic en Escritorio, los parámetros de búsqueda se pasan a Windows Desktop Search, que busca en el catálogo y muestra los resultados en la interfaz de usuario de WDS. Para que los usuarios inicien una búsqueda de escritorio desde las páginas web, wdsbho debe estar instalado y habilitado en sus sistemas, las páginas web deben estar registradas con WDS como una dirección URL permitida y debe crear un vínculo para pasar la consulta con el usuario a WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Habilitar el objeto de ayuda del explorador WDS

La BHO se instala y habilita en Internet Explorer de forma predeterminada al instalar WDS, pero puede comprobar fácilmente que no se ha deshabilitado ni desinstalado. En el sistema de un usuario, abra Internet Explorer ,  seleccione Opciones de **Internet** en el menú Herramientas, haga clic en la pestaña **Programas** y, a continuación, haga clic en **Administrar complementos.** En la lista de complementos, busque la clase dsWebAllowBHO y asegúrese de que está habilitada. Cuando la BHO está deshabilitada, WDS seguirá funcionando con normalidad; sin embargo, no podrá buscar en el escritorio desde una página web.

Las dos opciones siguientes para permitir una búsqueda de escritorio ejecutarán la búsqueda localmente con la aplicación de búsqueda registrada.

## <a name="registering-web-page-urls"></a>Registro de direcciones URL de página web

El Registro incluye una lista de direcciones URL de dominio "permitidas" desde las que se puede llamar a WDS. Para incluir las páginas web, debe enumerar las direcciones URL de dominio como REG SZ en el Registro como \_ se muestra a continuación:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **Allowed** \\ *&lt; number &gt;*  =  &lt; domainURL&gt;

Donde **&lt; number &gt;** se numera secuencialmente y **&lt; domainURL &gt;** es la dirección URL de la página web desde la que desea permitir búsquedas de WDS. Esta cadena de dirección URL puede incluir el asterisco \* comodín al principio o al final de la dirección URL. Por ejemplo, si la cadena es ".mydomain.com", puede iniciar una búsqueda \* de WDS desde https://www.mydomain.com y https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Habilitación de la búsqueda de escritorio por dirección URL

Otra opción que no requiere acceso al Registro es usar la siguiente dirección URL en las páginas web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

donde **QUERY** es la cadena codificada en URL en la que el usuario está buscando, incluidos los términos [de sintaxis de consulta](-search-2x-wds-aqsreference.md) avanzada.

 

 




