---
description: Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.
title: MLHtmlHelp función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997268"
---
# <a name="mlhtmlhelp-function"></a>MLHtmlHelp función)

\[Esta función está disponible a través de Windows XP y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndCaller* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana primaria que llama a esta función.

</dd> <dt>

*pszFile* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Un puntero a un búfer que contiene la ruta de acceso completa de un archivo de ayuda compilado (. chm) o un archivo de tema dentro de un archivo de ayuda especificado.

</dd> <dt>

*uCommand* \[ de\]
</dt> <dd>

Tipo: **uint**

Comando que se va a completar. Esta función solo admite directamente [el \_ \_ tema de presentación de HH](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) y el [ \_ \_ \_ menú emergente de texto para mostrar HH](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). En el caso de cualquier otro comando, la llamada se reenvía sin el valor de *dwCrossCodePage* a [htmlhelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ de\]
</dt> <dd>

Tipo: **DWORD \_ ptr**

Cualquier dato que sea necesario, en función del valor del parámetro *uCommand* .

</dd> <dt>

*dwCrossCodePage* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Valor **DWORD** que indica la página de códigos de la configuración actual del idioma de la interfaz de usuario, como CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **hWnd**

En función del *uCommand* especificado y del resultado, **MLHtmlHelp** devuelve uno de los siguientes elementos o ambos:

-   Identificador (HWND) de la ventana de ayuda.
-   **Null**. En algunos casos, **null** indica un error. en otros casos, **null** indica que aún no se ha creado la ventana de ayuda.

## <a name="remarks"></a>Observaciones

Si surge un problema con la ruta de acceso del archivo de ayuda para el idioma actual, la llamada se reenvía a [htmlhelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para el control estándar.

Cuando se cierra la ventana de ayuda, el foco vuelve al propietario a menos que el propietario sea el escritorio. Si *hwndCaller* es el escritorio, el sistema operativo determina dónde se devuelve el foco.

Además, si **MLHtmlHelp** envía mensajes de notificación desde la ventana de ayuda, los mensajes se envían a *hwndCaller* siempre que haya habilitado el seguimiento de [mensajes de notificación](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) en la definición de la ventana de ayuda.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se llama al comando [HH \_ Display \_ topic](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir el archivo de ayuda denominado help. chm y mostrar su tema predeterminado en la ventana de ayuda denominada `Mainwin` . Por lo general, la ventana de ayuda especificada en este comando es un [visor de ayuda HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)estándar.

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Al usar esta función, establezca el tamaño de la pila del archivo ejecutable de hospedaje en al menos 100.000. Si el tamaño de pila definido es demasiado pequeño, el subproceso creado para ejecutar la ayuda HTML también se creará con este tamaño de pila y se podría producir un error en la operación. Opcionalmente, puede quitar/STACK de la línea de comandos de vínculo y también quitar cualquier valor de la pila del archivo DEF del ejecutable (el tamaño de pila predeterminado es de 1 MB en este caso). También puede establecer el tamaño de la pila mediante el comando del compilador/Fnumber (el compilador lo pasará al enlazador como/STACK).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **MLHtmlHelpW** (Unicode) y **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
