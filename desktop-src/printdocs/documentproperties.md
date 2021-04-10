---
description: La función DocumentProperties recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Función DocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156756"
---
# <a name="documentproperties-function"></a>DocumentProperties (función)

La función **DocumentProperties** recupera o modifica la información de inicialización de la impresora o muestra una hoja de propiedades de configuración de impresora para la impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana primaria de la hoja de propiedades de configuración de la impresora.

</dd> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de un objeto de impresora. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pDeviceName* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del dispositivo para el que se muestra la hoja de propiedades de configuración de la impresora.

</dd> <dt>

*pDevModeOutput* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que recibe los datos de configuración de la impresora especificados por el usuario.

</dd> <dt>

*pDevModeInput* \[ de\]
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que el sistema operativo utiliza para inicializar los controles de la hoja de propiedades.

Este parámetro solo se usa si la marca **DM \_ in \_ buffer** está establecida en el parámetro *fMode* . Si no se establece **DM \_ in \_ buffer** , el sistema operativo utiliza el [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)predeterminado de la impresora.

</dd> <dt>

*fMode* \[ de\]
</dt> <dd>

Las operaciones que realiza la función. Si este parámetro es cero, la función **DocumentProperties** devuelve el número de bytes requeridos por la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) del controlador de la impresora. De lo contrario, use una o varias de las constantes siguientes para construir un valor para este parámetro; Tenga en cuenta, sin embargo, que para cambiar la configuración de impresión, una aplicación debe especificar al menos un valor de entrada y un valor de salida.



| Value                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <dt>**DM \_ en \_ búfer**</dt> </dl>    | Valor de entrada. Antes de solicitar, copiar o actualizar, la función combina la configuración de impresión actual del controlador de la impresora con la configuración de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada por el parámetro *pDevModeInput* . La función actualiza la estructura solo para los miembros especificados por el miembro **dmFields** de la estructura **DEVMODE** . Este valor también se define como **DM \_ Modify**. En casos de conflicto durante la combinación, la configuración de la estructura **DEVMODE** especificada por *pDevModeInput* invalida la configuración de impresión actual del controlador de la impresora.<br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <dt>**DM \_ en el \_ símbolo del sistema**</dt> </dl>    | Valor de entrada. La función presenta la hoja de propiedades de configuración de impresión del controlador de impresora y, a continuación, cambia la configuración de la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) de la impresora a los valores especificados por el usuario. Este valor también se define como **\_ prompt de DM**.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <dt>**búfer de DM \_ out \_**</dt> </dl> | Valor de salida. La función escribe la configuración de impresión actual del controlador de la impresora, incluidos los datos privados, en la estructura de datos [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) especificada por el parámetro *pDevModeOutput* . El autor de la llamada debe asignar un búfer lo suficientemente grande como para contener la información. Si los conjuntos **de \_ \_ búferes de DM out** están claros, el parámetro *pDevModeOutput* puede ser **null**. Este valor también se define como **\_ copia de DM**.<br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el parámetro *fMode* es cero, el valor devuelto es el tamaño del búfer necesario para contener los datos de inicialización del controlador de impresora. Tenga en cuenta que este búfer puede ser mayor que una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) si el controlador de impresora anexa datos privados a la estructura.

Si la función muestra la hoja de propiedades, el valor devuelto es **IDOK** o **IDCANCEL**, según el botón que seleccione el usuario.

Si la función no muestra la hoja de propiedades y es correcta, el valor devuelto es **IDOK**.

Si se produce un error en la función, el valor devuelto es menor que cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La cadena a la que apunta el parámetro *pDeviceName* se puede obtener llamando a la función [**GetPrinter**](getprinter.md) .

La estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) usada realmente por un controlador de impresora contiene la parte independiente del dispositivo (tal y como se definió anteriormente) seguida de una parte específica del controlador que varía en tamaño y contenido con cada controlador y versión del controlador. Debido a esta dependencia del controlador, es muy importante que las aplicaciones consulten al controlador el tamaño correcto de la estructura **DEVMODE** antes de asignar un búfer.

**Para realizar cambios en la configuración de impresión local para una aplicación, una aplicación debe seguir estos pasos:**

1.  Obtiene el número de bytes necesario para la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa llamando a **DocumentProperties** y especificando cero en el parámetro *fMode* .
2.  Asigne memoria para la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completa.
3.  Obtener la configuración actual de la impresora llamando a **DocumentProperties**. Pase un puntero a la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) asignada en el paso 2 como parámetro *pDevModeOutput* y especifique el valor del **búfer de DM \_ out \_** .
4.  Modifique los miembros adecuados de la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) devuelta e indique qué miembros se cambiaron estableciendo los bits correspondientes en el miembro **dmFields** de **DEVMODE**.
5.  Llame a **DocumentProperties** y pase la estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) modificada como parámetros *pDevModeInput* y *PDevModeOutput* y especifique los valores **de búfer DM \_ in \_ buffer** y **DM \_ out \_** (que se combinan mediante el operador OR). La estructura **DEVMODE** devuelta por la tercera llamada a **DocumentProperties** se puede usar como argumento en una llamada a la función [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .

Para crear un identificador para un contexto de dispositivo de impresora mediante la configuración actual de la impresora, solo tiene que llamar a **DocumentProperties** dos veces, tal y como se ha descrito anteriormente. La primera llamada obtiene el tamaño del [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) completo y la segunda llamada inicializa el **DEVMODE** con la configuración de la impresora actual. Pase el **DEVMODE** inicializado a [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) para obtener el identificador del contexto del dispositivo de impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DocumentPropertiesW** (Unicode) y **DocumentPropertiesA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AdvancedDocumentProperties**](advanceddocumentproperties.md)
</dt> <dt>

[**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

