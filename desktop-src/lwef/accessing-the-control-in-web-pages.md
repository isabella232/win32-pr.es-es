---
title: Obtener acceso al control en páginas web
description: Obtener acceso al control en páginas web
ms.assetid: 0c799c60-c81a-44ea-a9e0-1a385208528f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a965d73f7277b2b4a62c08a949782488f1e4dba4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790042"
---
# <a name="accessing-the-control-in-web-pages"></a>Obtener acceso al control en páginas web

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para tener acceso a los servicios del agente de Microsoft desde una página web, use la <OBJECT> etiqueta HTML dentro de la <HEAD> or <BODY> elemento de la página, especificando el CLSID (identificador de clase) de Microsoft para el control. Además, use un parámetro CODEBASE para especificar la ubicación del archivo de instalación del agente de Microsoft y su número de versión.

Si Microsoft Internet Explorer (versión 3,02 o posterior) está instalado en el sistema, pero aún no se ha instalado el agente de Microsoft y el usuario tiene acceso a una página web que tiene la <OBJECT> etiqueta con el CLSID del agente, el explorador intentará descargar automáticamente el agente desde el sitio web de Microsoft. A continuación, se pregunta al usuario si desea continuar con la instalación. En el caso de otros exploradores, póngase en contacto con el proveedor para obtener información sobre su soporte técnico o compatibilidad de terceros con los controles ActiveX.

En el ejemplo siguiente se muestra cómo usar el parámetro CODEBASE para descargar autodescarga del idioma Inglés versión 2,0 de Microsoft Agent.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

El agente también se puede instalar desde su propio servidor HTTP o como parte del proceso de instalación de una aplicación. Para admitir la instalación desde su propio servidor HTTP, debe publicar el archivo. cab de instalación automática de Microsoft Agent. Archivo exe y especifique su dirección URL en la etiqueta codebase.

``` syntax
<OBJECT
classid="clsid: D45FD31B-5C6E-11D1-9EC1-00C04FD7081F"
CODEBASE = "https://your server/msagent.exe#VERSION=2,0,0,0"
 id=Agent
>
</OBJECT>
```

Para admitir la descarga automática de un componente de idioma de agente de Microsoft desde una página web, incluya la etiqueta de objeto del componente de idioma en la página antes de la etiqueta de objeto de control del agente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID: C348XXXX-A7F8-11D1-AA75-00C04FA34D72"
CODEBASE = "#VERSION=2,0,0,0">
</OBJECT>
```

donde XXXX se reemplaza por un identificador de idioma. En el caso de los idiomas admitidos actualmente, consulte el sitio web del agente de Microsoft.

-   La <OBJECT> etiqueta de un componente de idioma debe preceder a la <OBJECT> etiqueta del componente principal de Microsoft Agent.
-   Se pueden instalar varios idiomas en el mismo cliente.
-   Antes de establecer el [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) de un carácter, se recomienda que el script Compruebe que la configuración regional del explorador, disponible en la propiedad [**userLanguage**](https://www.bing.com/search?q=**userLanguage**) , coincide con el idioma que se está estableciendo.

Para admitir otras versiones de idioma del agente, se usa otra etiqueta de objeto que especifica el componente de idioma. Sin embargo, tenga en cuenta que el intento de instalar varios idiomas al mismo tiempo puede requerir que el usuario se reinicie. Los componentes de idioma del agente pueden obtenerse del sitio web del agente mediante el mismo procedimiento que para el componente principal del agente. Las licencias de distribución para los componentes de idioma se describen en la licencia estándar de distribución de agentes. Para empezar a usar un carácter, debe cargar el carácter con el método [**Load**](/previous-versions/visualstudio/foxpro/h1tx7zt1(v=vs.71)) . Se puede cargar un carácter desde el almacenamiento local del usuario o un servidor HTTP. Para obtener más información sobre la sintaxis para cargar un carácter, vea el método **Load** . Una vez cargado el carácter correctamente, puede usar los métodos, las propiedades y los eventos expuestos por el control del agente para programar el carácter. También puede usar los métodos, las propiedades y los eventos expuestos por el lenguaje de programación y el explorador para programar el carácter; por ejemplo, para programar su reacción a un clic de botón. Consulte la documentación del explorador para determinar qué características expone en su modelo de scripting. Para Microsoft Internet Explorer, vea el modelo de objetos de scripting, que está disponible en el SDK de ActiveX.

Los servicios del agente permanecen cargados solo cuando hay al menos una aplicación cliente con una conexión. Esto significa que cuando un usuario se mueve entre páginas web habilitadas para el agente, el agente se cerrará y los caracteres que se carguen desaparecerán. Para mantener el agente en ejecución entre páginas (y, de este modo, mantener visible un carácter), cree otro cliente que permanezca cargado entre los cambios de la página. Por ejemplo, puede crear un cuadro de marcos HTML y declarar una <OBJECT> etiqueta para el agente en el marco primario. Después, puede incluir en el script las páginas que cargue en los fotogramas secundarios para llamar al script del elemento primario. También puede incluir una <OBJECT> etiqueta en cada página que se carga en el marco secundario. En este caso, recuerde que cada página será su propio cliente. Puede que tenga que usar el método [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) para establecer qué cliente tiene el control cuando el usuario interactúa con la página primaria o secundaria.

 

 