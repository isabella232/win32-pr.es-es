---
title: Implementar el objeto COM del menú contextual
description: Una extensión de menú contextual es un objeto COM implementado como un servidor en proceso.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- menú contextual objeto COM AD
- menú contextual objeto COM AD, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34d6b487d130327b379ed845f2d0157f2b28056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656334"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementar el objeto COM del menú contextual

Una extensión de menú contextual es un objeto COM implementado como un servidor en proceso. La extensión del menú contextual debe implementar las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) y [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Se crea una instancia de una extensión de menú contextual cuando el usuario muestra el menú contextual de un objeto de una clase para la que se ha registrado la extensión del menú contextual.

## <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

Después de crear una instancia del objeto COM de la extensión del menú contextual, se llama al método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **IShellExtInit:: Initialize** proporciona la extensión de menú contextual con un objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contiene los datos pertinentes para el objeto de directorio al que se aplica el menú contextual.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene datos en el formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . El formato de datos **\_ DSOBJECTNAMES de CFSTR** es un **HGLOBAL** que contiene una estructura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La estructura **DSOBJECTNAMES** contiene datos sobre el objeto de directorio al que se aplica la extensión de la hoja de propiedades.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) también contiene datos en el formato [**CFSTR \_ DS \_ Display \_ Spec \_ Options**](cfstr-ds-display-spec-options.md) . El formato de datos **CFSTR \_ DS \_ Display \_ Spec \_ Options** es un **HGLOBAL** que contiene una estructura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **DSDISPLAYSPECOPTIONS** contiene datos de configuración para su uso por la extensión.

Si se devuelve cualquier valor que no sea **\_ correcto** desde [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), no se utilizará la extensión del menú contextual.

No se usan los parámetros *pidlFolder* y *HkeyProgID* del método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .

## <a name="implementing-icontextmenu"></a>Implementación de IContextMenu

Después de que [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) devuelva, se llama al método [**IContextMenu:: QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para obtener el elemento de menú o los elementos que agregará la extensión del menú contextual. La implementación de **QueryContextMenu** es bastante sencilla. La extensión del menú contextual agrega sus elementos de menú mediante la función [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) o similar. Los identificadores de comando de menú deben ser mayores o iguales que *idCmdFirst* y deben ser menores que *idCmdLast*. **QueryContextMenu** debe devolver el identificador numérico más alto agregado al menú más uno. La mejor manera de asignar identificadores de comando de menú es comenzar por cero y subir en orden. Si la extensión del menú contextual no necesita ningún elemento de menú, simplemente no debe agregar ningún elemento al menú y devolver cero desde **QueryContextMenu**.

Se llama a [**IContextMenu:: GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) para recuperar datos de texto para el elemento de menú, como el texto de ayuda que se va a mostrar para el elemento de menú. Es posible que el host del menú contextual use cadenas Unicode, mientras que la extensión utiliza cadenas ANSI. Por este motivo, los casos de **GC \_ HELPTEXTA**, **GC \_ HELPTEXTW**, los **GC \_ verboa** y **GC \_ VERBW** deben administrarse individualmente. La implementación de este método es opcional.

Se llama a [**IContextMenu:: InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) cuando se selecciona uno de los elementos de menú instalados por la extensión del menú contextual. El menú contextual realiza o inicia las acciones deseadas en respuesta a este método.

 

 