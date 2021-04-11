---
description: La función GetPrinterDriver2 recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, GetPrinterDriver2 lo instala y muestra cualquier interfaz de usuario en la ventana especificada.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Función GetPrinterDriver2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279032"
---
# <a name="getprinterdriver2-function"></a>GetPrinterDriver2 función)

La función **GetPrinterDriver2** recupera los datos del controlador de la impresora especificada. Si el controlador no está instalado en el equipo local, **GetPrinterDriver2** lo instala y muestra cualquier interfaz de usuario en la ventana especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ en, opcional\]
</dt> <dd>

Identificador de la ventana que se usará como ventana primaria de cualquier interfaz de usuario, como un cuadro de diálogo, que el controlador muestra durante la instalación. Si el valor de este parámetro es **null**, la interfaz de usuario del controlador seguirá mostrándose al usuario durante la instalación, pero no tendrá una ventana primaria.

</dd> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que deben recuperarse los datos del controlador. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pEnvironment* \[ en, opcional\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el entorno (por ejemplo, Windows x86, Windows IA64 o Windows x64). Si este parámetro es **null**, se utiliza el entorno actual de la aplicación que realiza la llamada y el equipo cliente (no la aplicación de destino y el servidor de impresión).

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Estructura del controlador de impresora devuelta en el búfer de *pDriverInfo* . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                | Significado                                             |
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

Un puntero a un búfer que recibe una estructura que contiene información sobre el controlador, tal como se especifica en *LEVEL*. El búfer debe ser lo suficientemente grande como para almacenar las cadenas a las que apuntan los miembros de la estructura.

Para determinar el tamaño de búfer necesario, llame a **GetPrinterDriver2** con *cbBuf* establecido en cero. **GetPrinterDriver2** produce un error, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un **error de \_ \_ búfer insuficiente** y el parámetro *pcbNeeded* devuelve el tamaño, en bytes, del búfer necesario para contener la matriz de estructuras y sus datos.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Tamaño, en bytes, de la matriz en la que apunta *pDriverInfo* .

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Un puntero a un valor que recibe el número de bytes copiados si la función se ejecuta correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero. Para obtener el estado de retorno, llame a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Observaciones

Las [**estructuras \_ información \_**](driver-info-2.md)de controlador 2, información de [**controlador \_ \_ 3**](driver-info-3.md), [**información de controlador \_ \_ 4**](driver-info-4.md), [**información de controlador \_ \_ 5**](driver-info-5.md), [**información de controlador \_ \_ 6**](driver-info-6.md)e [**información de controlador \_ \_ 8**](driver-info-8.md) contienen el nombre de archivo o la ruta de acceso completa y el nombre de archivo del controlador de impresora en el miembro **pDriverPath** . Una aplicación puede usar la ruta de acceso y el nombre de archivo para cargar un controlador de impresora mediante una llamada a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y proporcionando la ruta de acceso y el nombre de archivo como argumento único.

La versión ANSI de esta función, **GetPrinterDriver2A** no se admite y devuelve un **error \_ no \_ compatible**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriver2W** (Unicode)<br/>                                                               |



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

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

