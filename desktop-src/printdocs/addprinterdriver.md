---
description: La función AddPrinterDriver instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Función AddPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815502"
---
# <a name="addprinterdriver-function"></a>AddPrinterDriver función)

La función **AddPrinterDriver** instala un controlador de impresora local o remoto y asocia los archivos de configuración, datos y controlador.

Para obtener más flexibilidad a la hora de instalar o actualizar controladores de impresora, use la función [**AddPrinterDriverEx**](addprinterdriverex.md) porque permite una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).

> [!Note]  
> Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) en su lugar.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el controlador.

Si *pName* es **null**, el controlador se instalará localmente.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Versión de la estructura a la que apunta *pDriverInfo* .

Este valor puede ser 2, 3, 4, 6 u 8.

</dd> <dt>

*pDriverInfo* \[ de\]
</dt> <dd>

Puntero a una estructura que contiene información del controlador de impresora. Esto depende del valor de *LEVEL*.



| Value | Estructura de unidad de impresora                  |
|-------|------------------------------------------|
| 2     | [**Información del controlador \_ \_ 2**](driver-info-2.md) |
| 3     | [**Información del controlador \_ \_ 3**](driver-info-3.md) |
| 4     | [**Información del controlador \_ \_ 4**](driver-info-4.md) |
| 6     | [**Información del controlador \_ \_ 6**](driver-info-6.md) |
| 8     | [**Información del controlador \_ \_ 8**](driver-info-8.md) |



 

Si el miembro **pEnvironment** de la estructura a la que apunta *pDriverInfo* es **null**, se usa el entorno actual del llamador o cliente (no del servidor de destino).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de que una aplicación llame a la función **AddPrinterDriver** , todos los archivos requeridos por el controlador deben copiarse en el directorio del controlador de impresora del sistema. Una aplicación puede recuperar el nombre de este directorio mediante una llamada a la función [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Una aplicación puede determinar qué controladores de impresora se instalan actualmente mediante una llamada a la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterDriverW** (Unicode) y **AddPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**Información del controlador \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**Información del controlador \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**Información del controlador \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**Información del controlador \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

