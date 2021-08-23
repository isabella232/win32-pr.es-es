---
description: La función GetPrinterDriverDirectory recupera la ruta de acceso del directorio printer-driver.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Función GetPrinterDriverDirectory (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4822f2478313dc902062ff907df5af3f0f7a515f19e414d2bc1534cc991b1ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971364"
---
# <a name="getprinterdriverdirectory-function"></a>Función GetPrinterDriverDirectory

La **función GetPrinterDriverDirectory** recupera la ruta de acceso del directorio printer-driver.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que reside el controlador de impresora. Si este parámetro es **NULL,** se recupera la ruta de acceso del directorio del controlador local.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **NULL,** se usa el entorno actual de la aplicación que realiza la llamada y la máquina cliente (no de la aplicación de destino ni del servidor de impresión).

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Nivel de estructura. Este valor debe ser 1.

</dd> <dt>

*pDriverDirectory* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la ruta de acceso.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño del búfer al que *apunta pDriverDirectory.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a un valor que especifica el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriverDirectoryW** (Unicode) y **GetPrinterDriverDirectoryA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> </dl>

 

 




