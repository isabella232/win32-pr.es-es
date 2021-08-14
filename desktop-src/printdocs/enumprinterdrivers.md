---
description: La función EnumPrinterDrivers enumera los controladores de impresora instalados en un servidor de impresora especificado.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Función EnumPrinterDrivers (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7be4efb1de46a960508972b00d113c5a27ab57187c1a89475eebcde69f14d978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686737"
---
# <a name="enumprinterdrivers-function"></a>Función EnumPrinterDrivers

La **función EnumPrinterDrivers** enumera los controladores de impresora instalados en un servidor de impresora especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que se enumeran los controladores de impresora.

Si *pName* es **NULL,** la función enumera los controladores de impresora locales.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno (por ejemplo, Windows x86, Windows IA64, Windows x64 o Windows NT R4000). Si este parámetro es **NULL,** la función usa el entorno actual del llamador o cliente (no del destino o servidor).

Si la *cadena pEnvironment* especifica "all", **EnumPrinterDrivers** enumera los controladores de impresora para todas las plataformas instaladas en el servidor especificado.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de estructura de información devuelta en el *búfer pDriverInfo.* Puede ser uno de los siguientes.



| Valor                                                                                                | Significado                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 1**](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 4**](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 5**](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMACIÓN \_ DEL \_ CONTROLADOR 8**](driver-info-8.md)<br/> |



 

</dd> <dt>

*pDriverInfo* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras DRIVER \_ \_ \* INFO, tal y como especifica level .  Cada estructura contiene datos que describen un controlador de impresora disponible. El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y las cadenas u otros datos a los que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumPrinterDrivers** con *cbBuf* establecido en cero. Se produce un error en **EnumPrinterDrivers,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pDriverInfo*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en el búfer *pDriverInfo* si la función se realiza correctamente. Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras devueltas en el *búfer pDriverInfo.* Este es el número de controladores de impresora instalados en el servidor de impresión especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrinterDriversW** (Unicode) y **EnumPrinterDriversA** (ANSI)<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 1**](driver-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 2**](driver-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 3**](driver-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 4**](driver-info-4.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 5**](driver-info-5.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 6**](driver-info-6.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

