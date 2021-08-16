---
description: Inicia Windows ayuda (Winhelp.exe) y pasa datos adicionales que indican la naturaleza de la ayuda solicitada por la aplicación.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: Función MLWinHelp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLWinHelp
- MLWinHelpA
- MLWinHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: a6c109f39107ba3cfd1800cca8db516d0033a2f3c32b9784e4359b3c6c50655d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968904"
---
# <a name="mlwinhelp-function"></a>Función MLWinHelp

\[Esta función está disponible a través Windows XP y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Inicia Windows ayuda (Winhelp.exe) y pasa datos adicionales que indican la naturaleza de la ayuda solicitada por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
BOOL MLWinHelp(
  _In_ HWND      hWndMain,
  _In_ LPCTSTR   lpszHelp,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWndMain* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana que solicita ayuda. La **función MLWinHelp** usa este identificador para realizar un seguimiento de las aplicaciones que han solicitado ayuda. Si el *parámetro uCommand* especifica HELP CONTEXTMENU o \_ HELP WM \_ \_ HELP, *hWndMain* identifica el control que solicita ayuda.

</dd> <dt>

*lpszHelp* \[ En\]
</dt> <dd>

Tipo: **LPCTSTR**

Dirección de una cadena terminada en NULL que contiene la ruta de acceso, si es necesario, y el nombre del archivo de ayuda que **mlwinhelp** va a mostrar.

El nombre de archivo puede ir seguido de un corchete angular (>) y el nombre de una ventana secundaria si el tema se va a mostrar en una ventana secundaria en lugar de en la ventana principal. Debe definir el nombre de la ventana secundaria en la sección WINDOWS del archivo \[ del proyecto de ayuda \] (.hpj).

</dd> <dt>

*uCommand* \[ En\]
</dt> <dd>

Tipo: **UINT**

Tipo de ayuda solicitada. Para obtener una lista de los valores posibles y cómo afectan al valor que se va a colocar en el *parámetro dwData,* vea la sección Comentarios.

</dd> <dt>

*dwData* \[ En\]
</dt> <dd>

Tipo: **DWORD \_ PTR**

Datos adicionales. El valor utilizado depende del valor del *parámetro uCommand.* Para obtener una lista de posibles *valores dwData,* consulte la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **BOOL**

Devuelve un valor distinto de cero si se ejecuta correctamente o cero en caso contrario. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función no se incluye en un archivo de encabezado y debe llamarse mediante ordinal 395 para **MLWinHelpA** y 397 para **MLWinHelpW.**

**MLWinHelp es** básicamente un contenedor para [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Intenta obtener la ruta de acceso al archivo de ayuda correspondiente a la configuración actual del lenguaje de interfaz de usuario antes de llamar **a WinHelp**. Si se realiza correctamente, pasa esa ruta de acceso. Si se produce un error, pasa la ruta de acceso a la que *apunta lpszHelp*.

Se produce un error en esta función si se llama desde cualquier contexto, pero el usuario actual.

Antes de cerrar la ventana que solicitó ayuda, la aplicación debe llamar a **MLWinHelp** con el *parámetro uCommand* establecido en HELP \_ QUIT. Hasta que todas las aplicaciones lo han hecho, Windows ayuda no finalizará. Tenga en cuenta que Windows ayuda con el comando HELP QUIT no es necesario si usó el comando \_ HELP CONTEXTPOPUP para iniciar Windows \_ Ayuda.

En la tabla siguiente se muestran los valores posibles para *el parámetro uCommand* y los formatos correspondientes del *parámetro dwData.*



| *uCommand*          | Acción                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| COMANDO \_ HELP       | Ejecuta una macro de ayuda o una cadena de macro.                                                                                                                                                                                                                               | Dirección de una cadena que especifica el nombre de las macros de ayuda que se ejecutarán. Si la cadena especifica varios nombres de macro, los nombres deben estar separados por punto y coma. Debe usar el formato corto del nombre de macro para algunas macros porque Windows Ayuda no admite el nombre largo.                         |
| CONTENIDO DE \_ AYUDA      | Muestra el tema especificado por la opción Contenido en la \[ sección OPTIONS del archivo \] .hpj. Este comando es por compatibilidad con versiones anteriores. Las nuevas aplicaciones deben proporcionar un archivo .cnt y usar el comando HELP \_ FINDER.                                           | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| CONTEXTO \_ DE AYUDA       | Muestra el tema identificado por el identificador de contexto especificado definido en la \[ sección MAP del archivo \] .hpj.                                                                                                                                                   | Contiene el identificador de contexto del tema.                                                                                                                                                                                                                                                               |
| HELP \_ CONTEXTMENU   | Muestra el **menú** Ayuda de la ventana seleccionada y, a continuación, muestra el tema del control seleccionado en una ventana emergente.                                                                                                                                             | Dirección de una matriz de **pares DWORD.** El primer **DWORD** de cada par es el identificador de control y el segundo es el identificador de contexto del tema. La matriz debe terminar con un par de {0,0} ceros. Si no desea agregar ayuda a un control determinado, establezca su identificador de contexto en -1. |
| HELP \_ CONTEXTPOPUP  | Muestra el tema identificado por el identificador de contexto especificado definido en la sección MAP del \[ \] archivo .hpj en una ventana emergente.                                                                                                                                | Contiene el identificador de contexto de un tema.                                                                                                                                                                                                                                                                 |
| BÚSQUEDA DE \_ AYUDA        | Muestra el cuadro **de diálogo Temas** de Ayuda.                                                                                                                                                                                                                             | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ FORCEFILE     | Garantiza que Windows ayuda muestra el archivo de ayuda correcto. Si se muestra el archivo de ayuda incorrecto, Windows Ayuda abre el correcto; De lo contrario, no hay ninguna acción.                                                                                     | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ HELPONHELP    | Muestra ayuda sobre cómo usar Windows ayuda, si el archivo Winhlp32.hlp está disponible.                                                                                                                                                                                     | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ INDEX         | Muestra el tema especificado por la opción Contenido en la \[ sección OPTIONS del archivo \] .hpj. Este comando es por compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar el comando \_ HELP FINDER.                                                                   | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| CLAVE \_ DE AYUDA           | Muestra el tema de la tabla de palabras clave que coincide con la palabra clave especificada, si hay una coincidencia exacta. Si hay más de una coincidencia, muestra el índice con los temas enumerados en el cuadro **de lista Temas** encontrados .                                                 | Dirección de una cadena de palabra clave. Varias palabras clave deben estar separadas por punto y coma.                                                                                                                                                                                                                              |
| HELP \_ MULTIKEY      | Muestra el tema especificado por una palabra clave en una tabla de palabras clave alternativas.                                                                                                                                                                                           | Dirección de una [**estructura MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que especifica un carácter de nota al pie de tabla y una palabra clave.                                                                                                                                                                                     |
| HELP \_ PARTIALKEY    | Muestra el tema de la tabla de palabras clave que coincide con la palabra clave especificada, si hay una coincidencia exacta. Si hay más de una coincidencia, muestra el cuadro **de diálogo Temas encontrados** . Para mostrar el índice sin pasar una palabra clave, use un puntero a una cadena vacía. | Dirección de una cadena de palabra clave. Varias palabras clave deben estar separadas por punto y coma.                                                                                                                                                                                                                              |
| HELP \_ QUIT          | Informa Windows ayuda de que ya no es necesaria. Si ninguna otra aplicación ha solicitado ayuda, Windows cerrará Windows Ayuda.                                                                                                                                         | Omitido; establecido en 0.                                                                                                                                                                                                                                                                                           |
| HELP \_ SETCONTENTS   | Especifica el tema Contenido. Windows La Ayuda muestra este tema cuando el usuario hace clic en el botón **Contenido** si el archivo de ayuda no tiene un archivo .cnt asociado.                                                                                                  | Contiene el identificador de contexto del tema Contenido.                                                                                                                                                                                                                                                      |
| HELP \_ SETPOPUP \_ POS | Establece la posición de la ventana emergente posterior.                                                                                                                                                                                                                   | Contiene los datos de posición. Use la [**macro MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) para concatenar las coordenadas horizontales y verticales en un solo valor. La ventana emergente se coloca como si el cursor del mouse estuviera en el punto especificado cuando se invocó la ventana emergente.                                 |
| HELP \_ SETWINPOS     | Muestra la Windows ayuda, si está minimizada o en memoria, y establece su tamaño y posición según lo especificado.                                                                                                                                                      | Dirección de una [**estructura HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) que especifica el tamaño y la posición de una ventana de ayuda principal o secundaria.                                                                                                                                                             |
| HELP \_ TCARD         | Indica que un comando es para una instancia de tarjeta de entrenamiento de Windows Ayuda. Combine este comando con otros comandos mediante el operador OR bit a bit.                                                                                                                    | Depende del comando con el que se combina este comando.                                                                                                                                                                                                                                                  |
| HELP \_ WM \_ HELP      | Muestra el tema para el control identificado por el *parámetro hWndMain* en una ventana emergente.                                                                                                                                                                        | Dirección de una matriz de **pares DWORD.** El primer **DWORD** de cada par es un identificador de control y el segundo es un identificador de contexto para un tema. La matriz debe terminar con un par de {0,0} ceros. Si no desea agregar ayuda a un control determinado, establezca su identificador de contexto en -1.       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5.0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **MLWinHelpW** (Unicode) y **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
