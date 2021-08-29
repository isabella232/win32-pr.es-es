---
description: La función EnumMonitors recupera información sobre los monitores de puerto instalados en el servidor especificado.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Función EnumMonitors (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 67a623e98b72ee26e6a9325120d26b26f92d03384318e90f28983a3a1978edf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949635"
---
# <a name="enummonitors-function"></a>Función EnumMonitors

La **función EnumMonitors** recupera información sobre los monitores de puerto instalados en el servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que residen los monitores. Si este parámetro es **NULL,** se enumeran los monitores locales.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que apunta *pMonitors.*

Este valor puede ser 1 o 2.

</dd> <dt>

*pMonitors* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que hacen referencia los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumMonitors** con *cbBuf* establecido en cero. Se produce un error en **EnumMonitors,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

El búfer recibe una matriz de [**estructuras MONITOR INFO \_ \_ 1**](monitor-info-1.md) si *Level* es 1 o [**MONITOR INFO \_ \_ 2**](monitor-info-2.md) si *Level* es 2.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pMonitors*.

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras devueltas en el búfer al que *apunta pMonitors.*

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
| Nombres Unicode y ANSI<br/>   | **EnumMonitorsW** (Unicode) y **EnumMonitorsA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**MONITOR \_ INFO \_ 1**](monitor-info-1.md)
</dt> <dt>

[**MONITOR \_ INFO \_ 2**](monitor-info-2.md)
</dt> </dl>

 

