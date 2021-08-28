---
description: La función EnumPrintProcessors enumera los procesadores de impresión instalados en el servidor especificado.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Función EnumPrintProcessors (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 800ed5afcf332a0c34dc272158f98fed64e47e86cb3c16cb24d6013951ffd3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846045"
---
# <a name="enumprintprocessors-function"></a>Función EnumPrintProcessors

La **función EnumPrintProcessors** enumera los procesadores de impresión instalados en el servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que residen los procesadores de impresión. Si este parámetro es **NULL,** se enumeran los procesadores de impresión locales.

</dd> <dt>

*pEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **NULL,** se usa el entorno actual de la aplicación que realiza la llamada y la máquina cliente (no de la aplicación de destino ni del servidor de impresión).

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de información devuelta en el *búfer pPrintProcessorInfo.* Este parámetro debe ser 1.

</dd> <dt>

*pPrintProcessorInfo* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras [**PRINTPROCESSOR \_ INFO \_ 1.**](printprocessor-info-1.md) Cada estructura describe un procesador de impresión disponible. El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumPrintProcessors** con *cbBuf* establecido en cero. Se produce un error en **EnumPrintProcessors,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPrintProcessorInfo.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en el búfer *pPrintProcessorInfo* si la función se realiza correctamente. Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras devueltas en el *búfer pPrintProcessorInfo.*

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
| Nombres Unicode y ANSI<br/>   | **EnumPrintProcessorsW** (Unicode) y **EnumPrintProcessorsA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**PRINTPROCESSOR \_ INFO \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

