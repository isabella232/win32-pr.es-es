---
description: La función AddPrintProcessor instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Función AddPrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678323"
---
# <a name="addprintprocessor-function"></a>AddPrintProcessor función)

La función **AddPrintProcessor** instala un procesador de impresión en el servidor especificado y agrega el nombre del procesador de impresión a la lista de procesadores de impresión admitidos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el procesador de impresión. Si este parámetro es **null**, el procesador de impresión se instala localmente.

</dd> <dt>

*pEnvironment* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **null**, se utiliza el entorno actual del llamador/cliente (no del destino/servidor).

</dd> <dt>

*pPathName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del archivo que contiene el procesador de impresión. Este archivo debe estar en el directorio del procesador de impresión del sistema.

</dd> <dt>

*pPrintProcessorName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de llamar a la función **AddPrintProcessor** , una aplicación debe comprobar que el archivo que contiene el procesador de impresión se almacena en el directorio del procesador de impresión del sistema. Una aplicación puede recuperar el nombre del directorio del procesador de impresión del sistema llamando a la función [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .

Una aplicación puede determinar el nombre de los procesadores de impresión existentes mediante una llamada a la función [**EnumPrintProcessors**](enumprintprocessors.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrintProcessorW** (Unicode) y **AddPrintProcessorA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

