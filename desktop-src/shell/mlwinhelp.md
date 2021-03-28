---
description: Inicia la ayuda de Windows (Winhelp.exe) y pasa datos adicionales que indican la naturaleza de la ayuda solicitada por la aplicación.
ms.assetid: e7466832-f236-4567-b05d-37d25fe88ba2
title: MLWinHelp función)
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
ms.openlocfilehash: badfeb599fd24fd255eb064bbaf6d99a3b758bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984603"
---
# <a name="mlwinhelp-function"></a>MLWinHelp función)

\[Esta función está disponible a través de Windows XP y Windows Server 2003. Podría modificarse o no estar disponible en versiones posteriores de Windows.\]

Inicia la ayuda de Windows (Winhelp.exe) y pasa datos adicionales que indican la naturaleza de la ayuda solicitada por la aplicación.

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

*hWndMain* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana que solicita ayuda. La función **MLWinHelp** usa este identificador para realizar un seguimiento de las aplicaciones que han solicitado ayuda. Si el parámetro *uCommand* especifica Help \_ CONTEXTMENU o Help \_ WM \_ Help, *hWndMain* identifica el control que solicita ayuda.

</dd> <dt>

*lpszHelp* \[ de\]
</dt> <dd>

Tipo: **LPCTSTR**

Dirección de una cadena terminada en null que contiene la ruta de acceso, si es necesario, y el nombre del archivo de ayuda que se va a mostrar en **MLWinHelp** .

El nombre de archivo puede ir seguido de un corchete angular (>) y el nombre de una ventana secundaria si el tema se va a mostrar en una ventana secundaria en lugar de en la ventana principal. Debe definir el nombre de la ventana secundaria en la \[ sección ventanas \] del archivo de proyecto de ayuda (. hpj).

</dd> <dt>

*uCommand* \[ de\]
</dt> <dd>

Tipo: **uint**

El tipo de ayuda solicitada. Para obtener una lista de los valores posibles y cómo afectan al valor que se va a colocar en el parámetro *dwData* , vea la sección Comentarios.

</dd> <dt>

*dwData* \[ de\]
</dt> <dd>

Tipo: **DWORD \_ ptr**

Datos adicionales. El valor utilizado depende del valor del parámetro *uCommand* . Para obtener una lista de posibles valores de *dwData* , consulte la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Devuelve un valor distinto de cero si se ejecuta correctamente o cero en caso contrario. Para obtener información de error extendida, llame a [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentarios

Esta función no se incluye en un archivo de encabezado y se debe llamar mediante el ordinal 395 para **MLWinHelpA** y 397 para **MLWinHelpW**.

**MLWinHelp** es esencialmente un contenedor para [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Intenta obtener la ruta de acceso al archivo de ayuda correspondiente a la configuración actual del idioma de la interfaz de usuario antes de llamar a **WinHelp**. Si se realiza correctamente, pasa la ruta de acceso. Si se produce un error, pasa la ruta de acceso a la que apunta *lpszHelp*.

Esta función genera un error si se llama desde cualquier contexto pero el usuario actual.

Antes de cerrar la ventana que solicitó la ayuda, la aplicación debe llamar a **MLWinHelp** con el parámetro *UCOMMAND* establecido en Help \_ Quit. Hasta que todas las aplicaciones hayan hecho esto, la ayuda de Windows no finalizará. Tenga en cuenta que llamar a la ayuda de Windows con el \_ comando help Quit no es necesario si ha usado el \_ comando help CONTEXTPOPUP para iniciar la ayuda de Windows.

En la tabla siguiente se muestran los posibles valores para el parámetro *uCommand* y los formatos correspondientes del parámetro *dwData* .



| *uCommand*          | Acción                                                                                                                                                                                                                                                               | *dwData*                                                                                                                                                                                                                                                                                                     |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_comando ayuda       | Ejecuta una macro de ayuda o una cadena de macro.                                                                                                                                                                                                                               | Dirección de una cadena que especifica el nombre de las macros de ayuda que se van a ejecutar. Si la cadena especifica varios nombres de macro, los nombres deben separarse con punto y coma. Debe usar la forma abreviada del nombre de la macro para algunas macros, ya que la ayuda de Windows no admite el nombre largo.                         |
| contenido de la ayuda \_      | Muestra el tema especificado por la opción contenido de la \[ \] sección de opciones del archivo. hpj. Este comando es para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben proporcionar un archivo. CNT y usar el \_ comando Finder de la ayuda.                                           | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| contexto de ayuda \_       | Muestra el tema identificado por el identificador de contexto especificado definido en la \[ \] sección Map del archivo. hpj.                                                                                                                                                   | Contiene el identificador de contexto para el tema.                                                                                                                                                                                                                                                               |
| AYUDA de \_ CONTEXTMENU   | Muestra el menú **ayuda** de la ventana seleccionada y, a continuación, muestra el tema del control seleccionado en una ventana emergente.                                                                                                                                             | Dirección de una matriz de pares **DWORD** . El primer **valor DWORD** de cada par es el identificador del control y el segundo es el identificador de contexto para el tema. La matriz debe terminar con un par de ceros {0,0} . Si no desea agregar ayuda a un control determinado, establezca el identificador de contexto en-1. |
| AYUDA \_ CONTEXTPOPUP  | Muestra el tema identificado por el identificador de contexto especificado definido en la \[ \] sección Map del archivo. hpj en una ventana emergente.                                                                                                                                | Contiene el identificador de contexto de un tema.                                                                                                                                                                                                                                                                 |
| buscador de ayuda \_        | Muestra el cuadro de diálogo **temas de ayuda** .                                                                                                                                                                                                                             | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| AYUDA \_ FORCEFILE     | Garantiza que la ayuda de Windows muestre el archivo de ayuda correcto. Si se muestra el archivo de ayuda incorrecto, la ayuda de Windows abre el correcto. de lo contrario, no hay ninguna acción.                                                                                     | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| AYUDA \_ HELPONHELP    | Muestra ayuda sobre cómo usar la ayuda de Windows, si el archivo WinHlp32. hlp está disponible.                                                                                                                                                                                     | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| Índice de la ayuda \_         | Muestra el tema especificado por la opción contenido de la \[ \] sección de opciones del archivo. hpj. Este comando es para la compatibilidad con versiones anteriores. Las nuevas aplicaciones deben usar el \_ comando Finder de la ayuda.                                                                   | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| tecla de ayuda \_           | Muestra el tema en la tabla de palabras clave que coincide con la palabra clave especificada, si hay una coincidencia exacta. Si hay más de una coincidencia, muestra el índice con los temas enumerados en el cuadro de lista **temas encontrados** .                                                 | Dirección de una cadena de palabra clave. Varias palabras clave deben estar separadas por punto y coma.                                                                                                                                                                                                                              |
| AYUDA \_ relaciones      | Muestra el tema especificado por una palabra clave en una tabla de palabras clave alternativa.                                                                                                                                                                                           | Dirección de una estructura [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que especifica un carácter de nota al pie de tabla y una palabra clave.                                                                                                                                                                                     |
| AYUDA \_ PARTIALKEY    | Muestra el tema en la tabla de palabras clave que coincide con la palabra clave especificada, si hay una coincidencia exacta. Si hay más de una coincidencia, muestra el cuadro de diálogo **temas encontrados** . Para mostrar el índice sin pasar una palabra clave, use un puntero a una cadena vacía. | Dirección de una cadena de palabra clave. Varias palabras clave deben estar separadas por punto y coma.                                                                                                                                                                                                                              |
| AYUDA \_ salir          | Informa a la ayuda de Windows de que ya no es necesaria. Si ninguna otra aplicación ha solicitado ayuda, Windows cierra la ayuda de Windows.                                                                                                                                         | Tendrán establézcalo en 0.                                                                                                                                                                                                                                                                                           |
| AYUDA \_ SETCONTENTS   | Especifica el tema de contenido. La ayuda de Windows muestra este tema cuando el usuario hace clic en el botón de **contenido** si el archivo de ayuda no tiene un archivo. CNT asociado.                                                                                                  | Contiene el identificador de contexto para el tema de contenido.                                                                                                                                                                                                                                                      |
| HELP \_ SETPOPUP \_ pos | Establece la posición de la ventana emergente siguiente.                                                                                                                                                                                                                   | Contiene los datos de la posición. Use la macro [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) para concatenar las coordenadas horizontal y vertical en un solo valor. La ventana emergente se coloca como si el cursor del mouse estuviera en el punto especificado cuando se invocó la ventana emergente.                                 |
| AYUDA \_ SETWINPOS     | Muestra la ventana de ayuda de Windows, si está minimizada o en memoria, y establece su tamaño y posición tal como se especificó.                                                                                                                                                      | Dirección de una estructura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) que especifica el tamaño y la posición de una ventana de ayuda primaria o secundaria.                                                                                                                                                             |
| AYUDA \_ TCARD         | Indica que un comando es para una instancia de tarjeta de entrenamiento de la ayuda de Windows. Combine este comando con otros comandos mediante el operador OR bit a bit.                                                                                                                    | Depende del comando con el que se combina este comando.                                                                                                                                                                                                                                                  |
| ayuda de WM de ayuda \_ \_      | Muestra el tema del control identificado por el parámetro *hWndMain* en una ventana emergente.                                                                                                                                                                        | Dirección de una matriz de pares **DWORD** . El primer **valor DWORD** de cada par es un identificador de control y el segundo es un identificador de contexto para un tema. La matriz debe terminar con un par de ceros {0,0} . Si no desea agregar ayuda a un control determinado, establezca el identificador de contexto en-1.       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>None</dt> </dl>                               |
| Archivo DLL<br/>                      | <dl> <dt>Shlwapi.dll (versión 5,0 o posterior)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **MLWinHelpW** (Unicode) y **MLWinHelpA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa)
</dt> <dt>

[**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa)
</dt> </dl>

 

 
