---
title: Implementar el objeto COM del menú contextual
description: Una extensión de menú contextual es un objeto COM implementado como un servidor en proceso.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- ad de objeto COM del menú contextual
- objeto COM del menú contextual AD , implementing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac371ea64239c18de2a8f30c969eb6d920221f0a802f18ceeebfef2c3991e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187653"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementar el objeto COM del menú contextual

Una extensión de menú contextual es un objeto COM implementado como un servidor en proceso. La extensión de menú contextual debe implementar las interfaces [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) [**e IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) Se crea una instancia de una extensión de menú contextual cuando el usuario muestra el menú contextual de un objeto de una clase para la que se ha registrado la extensión de menú contextual.

## <a name="implementing-ishellextinit"></a>Implementación de IShellExtInit

Una vez que se crea una instancia del objeto COM de extensión de menú contextual, se llama al método [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) **IShellExtInit::Initialize** proporciona a la extensión de menú contextual un objeto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) que contiene los datos pertinentes para el objeto de directorio al que se aplica el menú contextual.

[**IDataObject contiene**](/windows/win32/api/objidl/nn-objidl-idataobject) datos en formato [**CFSTR \_ DSOBJECTNAMES.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) El **formato de datos \_ DSOBJECTNAMES** de CFSTR es un **HGLOBAL** que contiene una [**estructura DSOBJECTNAMES.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) La **estructura DSOBJECTNAMES** contiene datos sobre el objeto de directorio al que se aplica la extensión de hoja de propiedades.

[**IDataObject también**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene datos en el formato [**CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) El **formato de datos \_ CFSTR DS \_ DISPLAY SPEC \_ \_ OPTIONS** es **un HGLOBAL** que contiene una [**estructura DSDISPLAYSPECOPTIONS.**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) **DSDISPLAYSPECOPTIONS** contiene datos de configuración para su uso por parte de la extensión.

Si se devuelve cualquier valor distinto de **S \_ OK** desde [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), no se usará la extensión de menú contextual.

No se usan los parámetros *pidlFolder* y *hkeyProgID* del método [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)

## <a name="implementing-icontextmenu"></a>Implementación de IContextMenu

Una vez que se devuelve [**IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) se llama al método [**IContextMenu::QueryContextMenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) para obtener el elemento de menú o los elementos que agregará la extensión de menú contextual. La **implementación queryContextMenu** es bastante sencilla. La extensión de menú contextual agrega sus elementos de menú mediante [**insertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) o una función similar. Los identificadores de comando de menú deben ser mayores o iguales que *idCmdFirst* y deben ser menores que *idCmdLast.* **QueryContextMenu debe** devolver el identificador numérico más grande agregado al menú más uno. La mejor manera de asignar identificadores de comandos de menú es empezar a cero y trabajar en secuencia. Si la extensión de menú contextual no necesita ningún elemento de menú, simplemente no debe agregar ningún elemento al menú y devolver cero desde **QueryContextMenu**.

[**Se llama a IContextMenu::GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) para recuperar datos textuales para el elemento de menú, como el texto de ayuda que se va a mostrar para el elemento de menú. Es posible que el host del menú contextual use cadenas Unicode mientras que la extensión usa cadenas ANSI. Por este problema, los **casos \_ HELPTEXTA,** **GCS \_ HELPTEXTW,** **GCS \_ VERBA** y **GCS \_ VERBW** deben controlarse individualmente. La implementación de este método es opcional.

[**Se llama a IContextMenu::InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) cuando se selecciona uno de los elementos de menú instalados por la extensión de menú contextual. El menú contextual realiza o inicia las acciones deseadas en respuesta a este método.

 

 