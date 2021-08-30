---
description: La función EnumPrintProcessorDatatypes enumera los tipos de datos que admite un procesador de impresión especificado.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Función EnumPrintProcessorDatatypes (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b6985181abca6fa6116fe39ab02ff5b60431bd44d771fedbcad179ba9e949a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091995"
---
# <a name="enumprintprocessordatatypes-function"></a>Función EnumPrintProcessorDatatypes

La **función EnumPrintProcessorDatatypes** enumera los tipos de datos que admite un procesador de impresión especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que reside el procesador de impresión. Si este parámetro es **NULL**, se enumeran los tipos de datos para el procesador de impresión local.

</dd> <dt>

*pPrintProcessorName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del procesador de impresión cuyos tipos de datos se enumeran.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de información devuelta en el búfer *pDatatypes.* Este parámetro debe ser 1.

</dd> <dt>

*pDatatypes* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de [**estructuras DATATYPES \_ INFO \_ 1.**](datatypes-info-1.md) Cada estructura describe un tipo de datos disponible. El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y las cadenas u otros datos a los que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumPrintProcessorDatatypes** con *cbBuf* establecido en cero. Se produce un error **en EnumPrintProcessorDatatypes,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que *apuntan los tipos pDatatypes*.

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en el búfer *pDatatypes* si la función se realiza correctamente. Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras devueltas en el *búfer pDatatypes.* Este es el número de tipos de datos admitidos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

v

A partir Windows Vista, la información del tipo de datos de los servidores de impresión remotos se recupera de una caché local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrintProcessorDatatypesW** (Unicode) y **EnumPrintProcessorDatatypesA** (ANSI)<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DATATYPES \_ INFO \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

