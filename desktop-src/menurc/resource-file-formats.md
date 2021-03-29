---
title: Formatos de archivo de recursos
description: En esta sección se describe el formato del archivo de recursos binario que crea el compilador de recursos basándose en el contenido del archivo de definición de recursos.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90c789cd1684c1f5ca31af0e2d60a31052ca03f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904593"
---
# <a name="resource-file-formats"></a>Formatos de archivo de recursos

En esta sección se describe el formato del archivo de recursos binario que crea el compilador de recursos basándose en el contenido del archivo de definición de recursos. Normalmente, este archivo tiene una extensión. res. El enlazador reformatea el archivo. res en un archivo de objeto de recurso y, a continuación, lo vincula al archivo ejecutable de una aplicación.

Un archivo de recursos binario se compone de una serie de entradas de recursos concatenadas. Cada entrada consta de un encabezado de recurso y de los datos de ese recurso. Un encabezado de recurso está alineado con **DWORD** en el archivo y consta de lo siguiente:

-   Un **valor DWORD** que contiene el tamaño del encabezado del recurso
-   **DWORD** que contiene el tamaño de los datos de recursos.
-   El tipo de recurso
-   Nombre del recurso
-   Información adicional de recursos

La estructura [**RESOURCEHEADER**](resourceheader.md) describe el formato de este encabezado. Los datos del recurso siguen el encabezado de recursos y son específicos de cada tipo de recurso. Algunos recursos también emplean una estructura de encabezado de grupo específica del recurso para proporcionar información sobre un grupo de recursos.

## <a name="accelerator-table-resources"></a>Recursos de tabla de aceleradores

Una tabla de aceleradores es una entrada de recurso en un archivo de recursos. No tiene un encabezado de grupo. Una estructura [**ACCELTABLEENTRY**](acceltableentry.md) describe cada entrada de la tabla de aceleradores. Se permiten varias tablas de aceleradores.

## <a name="cursor-and-icon-resources"></a>Recursos de cursor e icono

El sistema controla cada icono y cursor como un solo archivo. Sin embargo, estos se almacenan en archivos. res y en archivos ejecutables como un grupo de recursos de icono o un grupo de recursos de cursor. Los formatos de archivo de los recursos de icono y de cursor son similares. En el archivo. res, un encabezado de grupo de recursos sigue a todos los componentes de icono o de grupo de cursores individuales.

El formato de cada componente de icono es muy similar al formato del archivo. ico. Cada imagen de icono se almacena en una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , seguida de los bits de mapa de bits independientes del dispositivo (DIB) de color de la máscara **XOR** del icono. Los bits DIB monocromo de la máscara **y** del icono siguen los bits DIB de color.

El formato de cada componente de cursor es similar al formato del archivo. cur. Cada imagen de cursor se almacena en una estructura [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) , seguida de los bits DIB monocromo de la máscara **XOR** del cursor y, a continuación, los bits DIB monocromo de la máscara **y** del cursor. Tenga en cuenta que hay una diferencia en los mapas de bits de los dos recursos: a diferencia de los iconos, las máscaras XOR del cursor no tienen bits DIB de color. Aunque los mapas de bits de las máscaras de cursor son monocromo y no tienen encabezados DIB ni tablas de colores, los bits siguen en formato DIB con respecto a la alineación y dirección. Otra diferencia significativa entre los cursores y los iconos es que los cursores tienen una zona activa y los iconos no.

El encabezado de grupo para los recursos de icono y de cursor está formado por una estructura [**NEWHEADER**](newheader.md) más una o varias estructuras [**RESDIR**](resdir.md) . Hay una estructura **RESDIR** para cada icono o cursor. El encabezado de grupo contiene la información que necesita una aplicación para seleccionar el icono o cursor correcto que se va a mostrar. Tanto el encabezado de grupo como los datos que se repiten para cada icono o cursor del grupo tienen una longitud fija. Esto permite a la aplicación tener acceso a la información de forma aleatoria.

## <a name="dialog-box-resources"></a>Recursos del cuadro de diálogo

Un cuadro de diálogo también es una entrada de recurso en el archivo de recursos. Consta de una estructura de encabezado del cuadro de diálogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) más una estructura [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) para cada control del cuadro de diálogo. Las estructuras [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) y [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) describen el formato de los recursos extendidos del cuadro de diálogo.

## <a name="font-resources"></a>Recursos de fuentes

Las fuentes se almacenan en el archivo de recursos como un grupo de recursos. Las fuentes individuales componen un grupo de fuentes. Una instrucción de definición de recursos de la [instrucción de fuente](./font-statement.md) en. El archivo RC define cada fuente. Cada fuente individual del recurso se compone del contenido completo del archivo. FNT relacionado. Una estructura [**FONTGROUPHDR**](fontgrouphdr.md) sigue todos los componentes de fuente individuales del archivo. res.

Los recursos de fuente no se agregan a los recursos de una aplicación específica. En su lugar, normalmente se agregan a los archivos ejecutables que tienen la extensión. fon. Normalmente, estos archivos son archivos dll solo de recursos en lugar de aplicaciones.

## <a name="menu-resources"></a>Recursos de menú

Un *recurso de menú* se compone de una estructura [**MENUHEADER**](menuheader.md) seguida de una o varias estructuras [**NORMALMENUITEM**](normalmenuitem.md) o [**POPUPMENUITEM**](popupmenuitem.md) , una para cada elemento de menú de la plantilla de menú. El [**\_ \_ encabezado de plantilla MENUEX**](menuex-template-header.md) y las estructuras de [**\_ \_ elementos de plantilla MENUEX**](menuex-template-item.md) describen el formato de los recursos de menú extendidos.

## <a name="message-table-resources"></a>Recursos de tabla de mensajes

Una *tabla de mensajes* es un recurso que contiene texto con formato para mostrarlo como un mensaje de error o en un cuadro de mensaje. La estructura principal de un recurso de tabla de mensajes es la estructura de [**\_ \_ datos de recursos de mensaje**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) .

## <a name="version-resources"></a>Recursos de versión

La estructura principal de un recurso de versión es la estructura de [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Las estructuras adicionales incluyen la estructura [**VarFileInfo**](varfileinfo.md) para almacenar los datos de información de idioma y [**StringFileInfo**](stringfileinfo.md) para la información de cadena definida por el usuario. Todas las cadenas de un recurso de versión están en formato Unicode. Cada bloque de información se alinea en un límite **DWORD** .

 

 