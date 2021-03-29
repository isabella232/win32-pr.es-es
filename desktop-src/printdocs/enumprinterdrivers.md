---
description: La función EnumPrinterDrivers enumera los controladores de impresora instalados en un servidor de impresión especificado.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Función EnumPrinterDrivers (winspool. h)
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
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813550"
---
# <a name="enumprinterdrivers-function"></a>EnumPrinterDrivers función)

La función **EnumPrinterDrivers** enumera los controladores de impresora instalados en un servidor de impresión especificado.

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

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se enumeran los controladores de impresora.

Si *pName* es **null**, la función enumera los controladores de la impresora local.

</dd> <dt>

*pEnvironment* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64, Windows x64 o Windows NT R4000). Si este parámetro es **null**, la función utiliza el entorno actual del llamador/cliente (no del servidor de destino).

Si la cadena *pEnvironment* especifica "All", **EnumPrinterDrivers** enumera los controladores de impresora para todas las plataformas instaladas en el servidor especificado.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Tipo de estructura de información devuelto en el búfer de *pDriverInfo* . Puede ser uno de los siguientes.



| Value                                                                                                | Significado                                             |
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

Un puntero a un búfer que recibe una matriz de estructuras de información del controlador \_ \_ \* , tal como se especifica en *LEVEL*. Cada estructura contiene datos que describen un controlador de impresora disponible. El búfer debe ser lo suficientemente grande como para recibir la matriz de estructuras y cualquier cadena u otros datos a los que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **EnumPrinterDrivers** con *cbBuf* establecido en cero. **EnumPrinterDrivers** produce un error, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error \_ \_ de búfer insuficiente y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pDriverInfo*

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a una variable que recibe el número de bytes copiados en el búfer de *pDriverInfo* si la función se ejecuta correctamente. Si el búfer es demasiado pequeño, se produce un error en la función y la variable recibe el número de bytes necesarios.

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras devueltas en el búfer de *pDriverInfo* . Es el número de controladores de impresora instalados en el servidor de impresión especificado.

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
| Nombres Unicode y ANSI<br/>   | **EnumPrinterDriversW** (Unicode) y **EnumPrinterDriversA** (ANSI)<br/>                           |



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

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

