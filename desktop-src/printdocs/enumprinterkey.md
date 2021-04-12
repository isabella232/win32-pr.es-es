---
description: La función EnumPrinterKey enumera las subclaves de una clave especificada para una impresora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Función EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361098"
---
# <a name="enumprinterkey-function"></a>EnumPrinterKey función)

La función **EnumPrinterKey** enumera las subclaves de una clave especificada para una impresora especificada.

Los datos de la impresora se almacenan en el registro. Al enumerar los datos de la impresora, no llame a las funciones del registro que podrían cambiar los datos.

## <a name="syntax"></a>Sintaxis


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que la función enumera las subclaves. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pKeyName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica la clave que contiene las subclaves que se van a enumerar. Use el carácter de barra diagonal inversa \\ como delimitador para especificar una ruta de acceso con una o más subclaves. **EnumPrinterKey** enumera todas las subclaves de la clave, pero no enumera las subclaves de esas subclaves.

Si *pKeyName* es una cadena vacía (""), **EnumPrinterKey** enumera la clave de nivel superior de la impresora. Si *pKeyName* es **null**, **ENUMPRINTERKEY** devuelve un \_ parámetro de error no válido \_ .

</dd> <dt>

*pSubkey* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que recibe una matriz de nombres de subclave terminados en NULL. Dos caracteres nulos terminan la matriz.

</dd> <dt>

*cbSubkey* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pSubkey*. Si establece *cbSubkey* en cero, el parámetro *pcbSubkey* devuelve el tamaño de búfer necesario.

</dd> <dt>

*pcbSubkey* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes recuperados en el búfer de *pSubkey* . Si el tamaño de búfer especificado por *cbSubkey* es demasiado pequeño, la función devuelve un error \_ más \_ datos y *pcbSubkey* indica el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error del sistema. Si *pKeyName* no existe, el valor devuelto es el \_ archivo de error \_ no \_ encontrado.

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
| Nombres Unicode y ANSI<br/>   | **EnumPrinterKeyW** (Unicode) y **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




