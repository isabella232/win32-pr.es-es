---
description: La función GetPrintProcessorDirectory recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Función GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913154"
---
# <a name="getprintprocessordirectory-function"></a>GetPrintProcessorDirectory función)

La función **GetPrintProcessorDirectory** recupera la ruta de acceso al directorio del procesador de impresión en el servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor. Si este parámetro es **null**, se devuelve una ruta de acceso local.

</dd> <dt>

*pEnvironment* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Nivel de estructura. Este valor debe ser 1.

</dd> <dt>

*pPrintProcessorInfo* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe la ruta de acceso. Tenga en cuenta que, para los sistemas operativos anteriores a Windows Server 2003 SP 1, la ruta de acceso está en el formato local del servidor, no en el formato remoto real. Por ejemplo, la ruta de acceso se proporciona como "% WINDIR% \\ system32 \\ spool \\ Prtprocs \\ % Environment%" en lugar de " \\ \\ ServerName \\ Print $ \\ Prtprocs \\ % Environment%", incluso cuando se llama para un servidor remoto. En el caso de los sistemas operativos Windows Server 2003 SP 1 y versiones posteriores, se devuelve la ruta de acceso remota verdadera.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño del búfer al que apunta *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que especifica el número de bytes copiados si la función se ejecuta correctamente, o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

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
| Nombres Unicode y ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) y **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




