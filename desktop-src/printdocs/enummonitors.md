---
description: La función EnumMonitors recupera información acerca de los monitores de Puerto instalados en el servidor especificado.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Función EnumMonitors (winspool. h)
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
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813558"
---
# <a name="enummonitors-function"></a>EnumMonitors función)

La función **EnumMonitors** recupera información acerca de los monitores de Puerto instalados en el servidor especificado.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que residen los monitores. Si este parámetro es **null**, se enumeran los monitores locales.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Versión de la estructura a la que apunta *pMonitors*.

Este valor puede ser 1 o 2.

</dd> <dt>

*pMonitors* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de estructuras. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que hacen referencia los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **EnumMonitors** con *cbBuf* establecido en cero. **EnumMonitors** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

El búfer recibe una matriz de estructuras de supervisión de la [**\_ información \_ 1**](monitor-info-1.md) si el *nivel* es 1 o estructuras de [**supervisión de \_ información \_ 2**](monitor-info-2.md) si el *nivel* es 2.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pMonitors*.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras que se devolvieron en el búfer al que apunta *pMonitors*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumMonitorsW** (Unicode) y **EnumMonitorsA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Información de supervisión \_ \_ 1**](monitor-info-1.md)
</dt> <dt>

[**Información de supervisión \_ \_ 2**](monitor-info-2.md)
</dt> </dl>

 

