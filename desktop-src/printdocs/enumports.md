---
description: La función EnumPorts enumera los puertos disponibles para imprimir en un servidor especificado.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Función EnumPorts (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d1f5abc20e94c53e005ee97727a7de789f172bfef1d66703c72690910f197f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118056410"
---
# <a name="enumports-function"></a>Función EnumPorts

La **función EnumPorts** enumera los puertos disponibles para imprimir en un servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor cuyos puertos de impresora desea enumerar.

Si *pName* es **NULL,** la función enumera los puertos de impresora de la máquina local.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Tipo de información devuelta en el *búfer pPorts.* Si *Level* es 1, *pPorts* recibe una matriz de [**estructuras PORT INFO \_ \_ 1.**](port-info-1.md) Si *Level* es 2, *pPorts* recibe una matriz de [**estructuras PORT INFO \_ \_ 2.**](port-info-2.md)

</dd> <dt>

*pPorts* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras [**PORT \_ INFO \_ 1**](port-info-1.md) [**o PORT INFO \_ \_ 2.**](port-info-2.md) Cada estructura contiene datos que describen un puerto de impresora disponible. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame **a EnumPorts** con *cbBuf* establecido en cero. Se produce un error en **EnumPorts,** [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *byteNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPorts.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en el *búfer pPorts.* Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras [**\_ PORT INFO \_ 1**](port-info-1.md) o [**PORT INFO \_ \_ 2**](port-info-2.md) devueltas en el *búfer pPorts.* Este es el número de puertos de impresora que están disponibles en el servidor especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La **función EnumPorts** puede realizarse correctamente incluso si el servidor especificado por *pName* no tiene definida una impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPortsW** (Unicode) y **EnumPortsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**INFORMACIÓN \_ DE PUERTO \_ 1**](port-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DE PUERTO \_ 2**](port-info-2.md)
</dt> </dl>

 

