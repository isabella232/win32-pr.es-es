---
description: La función GetPrinterDriver recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, GetPrinterDriver lo instala.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Función GetPrinterDriver (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 0a20cd1dedb515714565c1e94f7847fdfc5c7969429686f17682b76cfef070e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971384"
---
# <a name="getprinterdriver-function"></a>Función GetPrinterDriver

La **función GetPrinterDriver** recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, **GetPrinterDriver** lo instala.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que se deben recuperar los datos del controlador. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **NULL,** se usa el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no de la aplicación de destino ni del servidor de impresión).

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Estructura del controlador de impresora devuelta en el *búfer pDriverInfo.* Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una estructura que contiene información sobre el controlador, tal y como especifica Level. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a GetPrinterDriver** con *cbBuf* establecido en cero. **GetPrinterDriver** produce un error, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz en la que *apunta pDriverInfo.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a un valor que recibe el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para un controlador inexistente, la función devuelve ERROR \_ UNKNOWN \_ PRINTER \_ DRIVER.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Las estructuras [**\_ DRIVER INFO \_ 2**](driver-info-2.md), [**DRIVER INFO \_ \_ 3,**](driver-info-3.md) [**DRIVER INFO \_ \_ 4**](driver-info-4.md), [**DRIVER INFO \_ \_ 5**](driver-info-5.md)y [**DRIVER INFO \_ \_ 6**](driver-info-6.md) contienen el nombre de archivo o la ruta de acceso completa y el nombre de archivo del controlador de impresora en el **miembro pDriverPath.** Una aplicación puede usar la ruta de acceso y el nombre de archivo para cargar un controlador de impresora llamando a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y suministrando la ruta de acceso y el nombre de archivo como argumento único.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriverW** (Unicode) y **GetPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 1**](driver-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 3**](driver-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 4**](driver-info-4.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 5**](driver-info-5.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

