---
description: La función EnumPorts enumera los puertos que están disponibles para imprimir en un servidor especificado.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Función EnumPorts (winspool. h)
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
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648511"
---
# <a name="enumports-function"></a>EnumPorts función)

La función **EnumPorts** enumera los puertos que están disponibles para imprimir en un servidor especificado.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor cuyos puertos de impresora se desea enumerar.

Si *pName* es **null**, la función enumera los puertos de impresora del equipo local.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Tipo de información que se devuelve en el búfer de *pPorts* . Si el *nivel* es 1, *pPorts* recibe una matriz de estructuras de [**información de puerto \_ \_ 1**](port-info-1.md) . Si *LEVEL* es 2, *pPorts* recibe una matriz de estructuras [**Port \_ info \_ 2**](port-info-2.md) .

</dd> <dt>

*pPorts* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe una matriz de estructuras de la [**información de puerto \_ \_ 1**](port-info-1.md) o de la [**información de puerto \_ \_ 2**](port-info-2.md) . Cada estructura contiene datos que describen un puerto de impresora disponible. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **EnumPorts** con *cbBuf* establecido en cero. **EnumPorts** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pPorts*.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en el búfer de *pPorts* . Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Un puntero a una variable que recibe el número de estructuras de [**información de puerto \_ \_ 1**](port-info-1.md) o de la [**información de puerto \_ \_ 2**](port-info-2.md) devueltas en el búfer de *pPorts* . Es el número de puertos de impresora que están disponibles en el servidor especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La función **EnumPorts** puede tener éxito incluso si el servidor especificado por *pName* no tiene una impresora definida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

[**Información de puerto \_ \_ 1**](port-info-1.md)
</dt> <dt>

[**INFO. de puerto \_ \_ 2**](port-info-2.md)
</dt> </dl>

 

