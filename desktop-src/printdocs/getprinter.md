---
description: La función GetPrinter recupera información sobre una impresora especificada.
ms.assetid: f162edbb-83ee-40c3-8710-9c867301d652
title: Función GetPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinter
- GetPrinterA
- GetPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: e99b3574762b84b830845da8149b0406664b6da7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707169"
---
# <a name="getprinter-function"></a>GetPrinter función)

La función **GetPrinter** recupera información sobre una impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetPrinter(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrinter,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que la función recupera información. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Nivel o tipo de estructura que la función almacena en el búfer al que apunta *pPrinter*.

Este valor puede ser 1, 2, 3, 4, 5, 6, 7, 8 o 9.

</dd> <dt>

*pPrinter* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe una estructura que contiene información sobre la impresora especificada. El búfer debe ser lo suficientemente grande como para recibir la estructura y las cadenas u otros datos a los que apuntan los miembros de la estructura. Si el búfer es demasiado pequeño, el parámetro *pcbNeeded* devuelve el tamaño de búfer necesario.

El tipo de estructura viene determinado por el valor de *LEVEL*.



| Nivel                                                                                                | Estructura                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 1**](printer-info-1.md) que contiene información general de la impresora.<br/>                                                                                                        |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información detallada acerca de la impresora.<br/>                                                                                             |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 3**](printer-info-3.md) que contiene la información de seguridad de la impresora.<br/>                                                                                                 |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 4**](printer-info-4.md) que contiene la información de impresora mínima, incluido el nombre de la impresora, el nombre del servidor y si la impresora es remota o local.<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Una estructura de información de impresora [**\_ \_ 5**](printer-info-5.md) que contiene información de la impresora, como los atributos de impresora y la configuración de tiempo de espera.<br/>                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Estructura de la información de la [**impresora \_ \_ 6**](printer-info-6.md) que especifica el valor de estado de una impresora.<br/>                                                                                                      |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 7**](printer-info-7.md) que indica si la impresora está publicada en el servicio de directorio.<br/>                                                                      |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | Una estructura de la información de la [**impresora \_ \_ 8**](printer-info-8.md) que especifica la configuración de impresora predeterminada global.<br/>                                                                                                |
| <span id="9"></span><dl> <dt>**9**</dt> </dl> | Una estructura de [**información de impresora \_ \_ 9**](printer-info-9.md) que especifica la configuración de impresora predeterminada por usuario.<br/>                                                                                              |



 

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPrinter*.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que la función establece en el tamaño, en bytes, de la información de la impresora. Si *cbBuf* es menor que este valor, **GetPrinter** produce un error y el valor representa el tamaño de búfer necesario. Si *cbBuf* es igual o mayor que este valor, **GetPrinter** se realiza correctamente y el valor representa el número de bytes almacenados en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El miembro **pDevMode** de las estructuras [**Printer info \_ \_ 2**](printer-info-2.md), [**Printer \_ info \_ 8**](printer-info-8.md)y [**Printer \_ info \_ 9**](printer-info-9.md) puede ser **null**. Cuando esto sucede, la impresora no se puede usar hasta que el controlador se vuelve a instalar correctamente.

En el caso de las estructuras [**Printer \_ info \_ 2**](printer-info-2.md) y [**Printer \_ info \_ 3**](printer-info-3.md) que contienen un puntero a un descriptor de seguridad, la función solo recupera los componentes del descriptor de seguridad para los que el autor de la llamada tiene permiso de lectura. Para recuperar determinados componentes de descriptor de seguridad, debe especificar los derechos de acceso necesarios cuando llame a la función [**OpenPrinter**](openprinter.md) para recuperar un identificador de la impresora. En la tabla siguiente se muestran los derechos de acceso necesarios para leer los distintos componentes de descriptor de seguridad.



| Derecho de acceso                        | Componente de descriptor de seguridad                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| CONTROL de lectura \_<br/>            | Propietario<br/> Grupo primario<br/> Lista de control de acceso discrecional (DACL)<br/> |
| ACCESO a la \_ seguridad del sistema \_<br/> | Lista de control de acceso del sistema (SACL)<br/>                                                  |



 

Si especifica el nivel 7, el miembro **dwAction** de la información de la [**impresora \_ \_ 7**](printer-info-7.md) devuelve uno de los siguientes valores para indicar si la impresora está publicada en el servicio de directorio.



| valor dwAction     | Significado                                                                                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| publicación de DSPRINT \_   | La impresora está publicada. El miembro **pszObjectGUID** contiene el GUID del objeto cola de impresión de servicios de directorio asociado a la impresora.                                                                                                       |
| DSPRINT \_ Anular publicación | La impresora no está publicada.                                                                                                                                                                                                                            |
| DSPRINT \_ pendiente   | Indica que el sistema está intentando completar una operación de publicación o anulación de publicación. Si una llamada a [**SetPrinter**](setprinter.md) no puede publicar o anular la publicación de una impresora, el sistema realiza más intentos para completar la operación en segundo plano. |



 

A partir de Windows Vista, los datos de la impresora devueltos por **GetPrinter** se recuperan de una caché local cuando *hPrinter* hace referencia a una impresora hospedada por un servidor de impresión y hay al menos una conexión abierta con el servidor de impresión. En todas las demás configuraciones, los datos de la impresora se consultan desde el servidor de impresión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterW** (Unicode) y **GetPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AbortPrinter**](abortprinter.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**Información de la impresora \_ \_ 5**](printer-info-5.md)
</dt> <dt>

[**Información de la impresora \_ \_ 7**](printer-info-7.md)
</dt> <dt>

[**Información de la impresora \_ \_ 8**](printer-info-8.md)
</dt> <dt>

[**Información de la impresora \_ \_ 9**](printer-info-9.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

 




