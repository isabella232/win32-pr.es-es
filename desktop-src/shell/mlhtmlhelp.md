---
description: Muestra una ventana de ayuda que corresponde a la configuración actual del idioma de la interfaz de usuario.
title: Función MLHtmlHelp
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
ms.openlocfilehash: c38e84df2ca6f379e7d479125f1f454a10426406ba40ad21721fe01f67cce6f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090215"
---
# <a name="mlhtmlhelp-function"></a>Función MLHtmlHelp

\[Esta función está disponible a través Windows XP y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

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

*hwndCaller* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana primaria que llama a esta función.

</dd> <dt>

*pszFile* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Puntero a un búfer que contiene la ruta de acceso completa de un archivo de ayuda compilado (.chm) o un archivo de tema dentro de un archivo de ayuda especificado.

</dd> <dt>

*uCommand* \[ En\]
</dt> <dd>

Tipo: **UINT**

Comando que se completará. Esta función solo admite directamente [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) y [HH DISPLAY TEXT \_ \_ \_ POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command). En el caso de cualquier otro comando, la llamada se reenvía sin el valor *dwCrossCodePage* a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).

</dd> <dt>

*dwData* \[ En\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Cualquier dato que pueda ser necesario, en función del valor del *parámetro uCommand.*

</dd> <dt>

*dwCrossCodePage* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Valor **DWORD que** indica la página de códigos de la configuración actual del idioma de la interfaz de usuario, como CP \_ ACP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HWND**

Según el *uCommand* y el resultado especificados, **MLHtmlHelp** devuelve uno o ambos de los siguientes elementos:

-   Identificador (hwnd) de la ventana de ayuda.
-   **NULL.** En algunos casos, **NULL** indica un error; En otros casos, **NULL** indica que aún no se ha creado la ventana de ayuda.

## <a name="remarks"></a>Comentarios

Si surge un problema con la ruta de acceso del archivo de ayuda para el lenguaje actual, la llamada se reenvía a [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) para el control estándar.

Cuando se cierra la ventana de ayuda, el foco vuelve al propietario a menos que el propietario sea el escritorio. Si *hwndCaller es* el escritorio, el sistema operativo determina dónde se devuelve el foco.

Además, si **MLHtmlHelp** envía mensajes de notificación desde la ventana de ayuda, los mensajes [](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) se envían a *hwndCaller* siempre que haya habilitado el seguimiento de mensajes de notificación en la definición de la ventana de ayuda.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se llama al comando [HH \_ DISPLAY \_ TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) para abrir el archivo de ayuda denominado Help.chm y mostrar su tema predeterminado en la ventana de ayuda denominada `Mainwin` . Por lo general, la ventana de ayuda especificada en este comando es un Visor de [Ayuda HTML estándar.](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics)

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> Al usar esta función, establezca el tamaño de pila del ejecutable de hospedaje en al menos 100 000. Si el tamaño de pila definido es demasiado pequeño, el subproceso creado para ejecutar la Ayuda HTML también se creará con este tamaño de pila y se podría producir un error en la operación. Opcionalmente, puede quitar /STACK de la línea de comandos del vínculo y también quitar cualquier configuración STACK en el archivo DEF del ejecutable (el tamaño de pila predeterminado es 1 MB en este caso). También puede establecer el tamaño de pila mediante el comando del compilador /Fnumber (el compilador lo pasará al vinculador como /STACK).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **MLHtmlHelpW** (Unicode) y **MLHtmlHelpA** (ANSI)<br/>                                               |



 

 
