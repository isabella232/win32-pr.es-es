---
description: La función GetPrinterDriver recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, GetPrinterDriver lo instala.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Función GetPrinterDriver (winspool. h)
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
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707231"
---
# <a name="getprinterdriver-function"></a>GetPrinterDriver función)

La función **GetPrinterDriver** recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, **GetPrinterDriver** lo instala.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que deben recuperarse los datos del controlador. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pEnvironment* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Estructura del controlador de impresora devuelta en el búfer de *pDriverInfo* . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**Información del controlador \_ \_ 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Información del controlador \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Información del controlador \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Información del controlador \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**Información del controlador \_ \_ 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Información del controlador \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Información del controlador \_ \_ 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una estructura que contiene información sobre el controlador, tal como se especifica en Level. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **GetPrinterDriver** con *cbBuf* establecido en cero. **GetPrinterDriver** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz en la que apunta *pDriverInfo* .

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Para un controlador no existente, la función devuelve el ERROR \_ \_ controlador de impresora desconocido \_ .

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Las estructuras [**driver \_ info \_ 2**](driver-info-2.md), info. de controlador [**\_ \_ 3**](driver-info-3.md), info. de controlador [**\_ \_ 4**](driver-info-4.md), info. de controlador [**\_ \_ 5**](driver-info-5.md)y [**driver \_ info \_ 6**](driver-info-6.md) contienen el nombre de archivo o la ruta de acceso completa y el nombre de archivo del controlador de impresora en el miembro **pDriverPath** . Una aplicación puede usar la ruta de acceso y el nombre de archivo para cargar un controlador de impresora mediante una llamada a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y proporcionando la ruta de acceso y el nombre de archivo como argumento único.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriverW** (Unicode) y **GetPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**Información del controlador \_ \_ 1**](driver-info-1.md)
</dt> <dt>

[**Información del controlador \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**Información del controlador \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**Información del controlador \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**Información del controlador \_ \_ 5**](driver-info-5.md)
</dt> <dt>

[**Información del controlador \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

