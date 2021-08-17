---
title: Formatos de archivo de recursos
description: En esta sección se describe el formato del archivo de recursos binarios que crea el compilador de recursos en función del contenido del archivo de definición de recursos.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869796"
---
# <a name="resource-file-formats"></a>Formatos de archivo de recursos

En esta sección se describe el formato del archivo de recursos binarios que crea el compilador de recursos en función del contenido del archivo de definición de recursos. Este archivo normalmente tiene una extensión .res. El vinculador vuelve a formatear el archivo .res en un archivo de objeto de recurso y, a continuación, lo vincula al archivo ejecutable de una aplicación.

Un archivo de recursos binario consta de varias entradas de recursos concatenadas. Cada entrada consta de un encabezado de recurso y los datos de ese recurso. Un encabezado de recurso está alineado con **DWORD** en el archivo y consta de lo siguiente:

-   DWORD **que** contiene el tamaño del encabezado de recurso
-   DWORD **que** contiene el tamaño de los datos de recursos
-   El tipo de recurso
-   Nombre del recurso
-   Información adicional de recursos

La [**estructura RESOURCEHEADER**](resourceheader.md) describe el formato de este encabezado. Los datos del recurso siguen el encabezado del recurso y son específicos de cada tipo de recurso. Algunos recursos también emplean una estructura de encabezado de grupo específica del recurso para proporcionar información sobre un grupo de recursos.

## <a name="accelerator-table-resources"></a>Recursos de tabla de aceleradores

Una tabla de aceleradores es una entrada de recursos en un archivo de recursos. No tiene un encabezado de grupo. Una [**estructura ACCELTABLEENTRY**](acceltableentry.md) describe cada entrada de la tabla de aceleradores. Se permiten varias tablas de aceleradores.

## <a name="cursor-and-icon-resources"></a>Recursos de cursor e icono

El sistema controla cada icono y cursor como un único archivo. Sin embargo, se almacenan en archivos .res y en archivos ejecutables como un grupo de recursos de icono o un grupo de recursos de cursor. Los formatos de archivo de los recursos de icono y cursor son similares. En el archivo .res, un encabezado de grupo de recursos sigue todos los componentes individuales del icono o del grupo de cursores.

El formato de cada componente de icono se parece mucho al formato del archivo .ico. Cada imagen de icono se almacena en una estructura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida de los bits de mapa de bits independientes del dispositivo (DIB) de color de la máscara **XOR del** icono. Los bits DIB monocromáticos de la máscara **AND** del icono siguen los bits DIB de color.

El formato de cada componente de cursor es similar al formato del archivo .cur. Cada imagen de cursor se almacena en una estructura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguida de los bits DIB monocromáticos de la máscara **XOR** del cursor y, a continuación, por los bits DIB monocromáticos de la máscara **AND** del cursor. Tenga en cuenta que hay una diferencia en los mapas de bits de los dos recursos: a diferencia de los iconos, las máscaras XOR de cursor no tienen bits DIB de color. Aunque los mapas de bits de las máscaras de cursor son monocromáticos y no tienen encabezados DIB ni tablas de colores, los bits siguen en formato DIB con respecto a la alineación y la dirección. Otra diferencia significativa entre los cursores y los iconos es que los cursores tienen una zona activa y los iconos no.

El encabezado de grupo para los recursos de icono y cursor consta de una [**estructura NEWHEADER**](newheader.md) más una o varias estructuras [**RESDIR.**](resdir.md) Hay una estructura **RESDIR** para cada icono o cursor. El encabezado de grupo contiene la información que una aplicación necesita para seleccionar el icono o cursor correctos que se mostrarán. Tanto el encabezado de grupo como los datos que se repiten para cada icono o cursor del grupo tienen una longitud fija. Esto permite que la aplicación acceda aleatoriamente a la información.

## <a name="dialog-box-resources"></a>Recursos del cuadro de diálogo

Un cuadro de diálogo también es una entrada de recurso en el archivo de recursos. Consta de una estructura de encabezado de cuadro de diálogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) más una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) para cada control del cuadro de diálogo. Las [**estructuras DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) y [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) describen el formato de los recursos extendidos del cuadro de diálogo.

## <a name="font-resources"></a>Recursos de fuentes

Las fuentes se almacenan en el archivo de recursos como un grupo de recursos. Las fuentes individuales son un grupo de fuentes. Una [instrucción de definición de](./font-statement.md) recursos de instrucción FONT en . El archivo RC define cada fuente. Cada fuente individual del recurso consta del contenido completo del archivo .fnt relacionado. Una [**estructura FONTGROUPHDR**](fontgrouphdr.md) sigue todos los componentes de fuente individuales del archivo .res.

Los recursos de fuente no se agregan a los recursos de una aplicación específica. En su lugar, normalmente se agregan a los archivos ejecutables que tienen una extensión .fon. Normalmente, estos archivos son archivos DLL solo de recursos en lugar de aplicaciones.

## <a name="menu-resources"></a>Recursos de menú

Un *recurso de menú* consta de una estructura [**MENUHEADER**](menuheader.md) seguida de una o varias estructuras [**NORMALMENUITEM**](normalmenuitem.md) o [**POPUPMENUITEM,**](popupmenuitem.md) una para cada elemento de menú de la plantilla de menú. Las [**estructuras MENUEX \_ TEMPLATE HEADER \_ y**](menuex-template-header.md) [**MENUEX TEMPLATE \_ \_ ITEM**](menuex-template-item.md) describen el formato de los recursos de menú extendidos.

## <a name="message-table-resources"></a>Recursos de tabla de mensajes

Una *tabla de mensajes* es un recurso que contiene texto con formato para mostrarse como un mensaje de error o en un cuadro de mensaje. La estructura principal de un recurso de tabla de mensajes es [**la estructura MESSAGE RESOURCE \_ \_ DATA.**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data)

## <a name="version-resources"></a>Recursos de versión

La estructura principal de un recurso de versión es [**la \_ estructura FIXEDFILEINFO de VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Entre las estructuras adicionales se [**incluyen la estructura VarFileInfo**](varfileinfo.md) para almacenar datos de información de lenguaje y [**StringFileInfo**](stringfileinfo.md) para la información de cadena definida por el usuario. Todas las cadenas de un recurso de versión están en formato Unicode. Cada bloque de información se alinea en un **límite DWORD.**

 

 