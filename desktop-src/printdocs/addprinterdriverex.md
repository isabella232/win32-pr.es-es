---
description: La función AddPrinterDriverEx instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Función AddPrinterDriverEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677730"
---
# <a name="addprinterdriverex-function"></a>AddPrinterDriverEx función)

La función **AddPrinterDriverEx** instala un controlador de impresora local o remota y vincula los archivos de configuración, datos y controlador. Además de tener las funcionalidades de [**AddPrinterDriver**](addprinterdriver.md), también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia de archivos más recientes solamente y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).

> [!Note]  
> Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) en su lugar.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar el controlador. Si este parámetro es **null**, la función instala el controlador en el equipo local.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Versión de la estructura a la que apunta *pDriverInfo* . Este valor puede ser 2, 3, 4, 6 u 8.

</dd> <dt>

*pDriverInfo* \[ in, out\]
</dt> <dd>

Puntero a una estructura que contiene información del controlador de impresora. Puede ser uno de los siguientes.



| Valor de nivel                                                                                       | \_Estructura de información del controlador \_ \*                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**Información del controlador \_ \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**Información del controlador \_ \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**Información del controlador \_ \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**Información del controlador \_ \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**Información del controlador \_ \_ 8**](driver-info-8.md)<br/> |



 

Si el miembro **pEnvironment** de la estructura a la que apunta *pDriverInfo* es **null**, la función usa el entorno actual del llamador o el cliente, no el entorno del servidor de destino.

</dd> <dt>

*dwFileCopyFlags* \[ de\]
</dt> <dd>

Opciones para copiar los archivos del controlador. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**APD \_ copiar \_ todos \_ los archivos**</dt> </dl>                | Agregue el controlador de impresora y copie todos los archivos en el directorio Printer-driver. Las marcas de tiempo de archivo se omiten con esta opción.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**APD \_ copiar \_ desde el \_ directorio**</dt> </dl> | Agregue el controlador de impresora con los nombres de archivo completos especificados en la estructura de [**información de controlador \_ \_ 6**](driver-info-6.md) . Esta marca es ORed junto con una de las otras marcas de copia. Si se establece esta marca, **AddPrinterDriverEx** producirá un error si los archivos no existen donde se especifica que existen en la estructura de **información de controlador \_ \_ 6** . No es necesario que los archivos se copien en el directorio del controlador de impresora del sistema. Vea la sección Comentarios.<br/> **Windows 2000:** Esta marca no se admite.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**APD \_ copiar \_ \_ archivos nuevos**</dt> </dl>                | Agregue el controlador de impresora y copie los archivos en el directorio de controlador de impresora que son más recientes que los archivos correspondientes que se están usando actualmente. Esta marca emula el comportamiento de [**AddPrinterDriver**](addprinterdriver.md).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**\_degradación estricta de APD \_**</dt> </dl>           | Agregue el controlador de impresora sólo si todos los archivos del directorio de controladores de impresora son más antiguos que los archivos correspondientes que se estén usando.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**\_actualización estricta de APD \_**</dt> </dl>                 | Agregue el controlador de impresora sólo si todos los archivos del directorio de controladores de impresora son más recientes que los archivos correspondientes actualmente en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Si se sabe que el controlador de impresora tiene problemas para trabajar con el sistema operativo, **AddPrinterDriverEx** producirá un error con uno de los siguientes códigos de error:



| Código de error                      | Significado                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| controlador de impresora de ERROR \_ \_ \_ bloqueado | El controlador no funciona en el sistema operativo.                                                                                                         |
| \_Advertencia de \_ controlador de impresora de error \_  | El controlador no es confiable en el sistema operativo. Sin embargo, si \_ \_ \_ se especifica APD instalar el controlador de advertencias, el controlador está instalado y no se proporciona ninguna advertencia. |



 

Para obtener más información, vea la sección Notas.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de llamar a la función **AddPrinterDriverEx** , todos los archivos requeridos por el controlador se deben copiar en el directorio de controladores de impresora del sistema. Para recuperar el nombre de este directorio, llame a la función [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Para determinar qué controladores de impresora están instalados actualmente, llame a la función [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Si el controlador de impresora se ha agregado correctamente, la función llama a la función DrvDriverEvent (controlador de \_ eventos \_ inicializados, nivel, información de controlador \_ \_ \* , lParam) para permitir que el controlador realice las inicializaciones necesarias durante la instalación de un controlador de impresora. Para obtener más información acerca de **DrvDriverEvent**, consulte el kit de desarrollo de controladores de Microsoft Windows (DDK)

El controlador no debe usar una llamada de interfaz de usuario durante la llamada a **DrvDriverEvent**. Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada VendorSetup en el archivo. inf de la impresora o, para Plug and Play dispositivos, el instalador puede usar un Coinstalador específico del dispositivo. Para obtener más información sobre VendorSetup, consulte el DDK.

Los archivos a los que se hace referencia en la estructura de la [**información de controlador \_ \_ 6**](driver-info-6.md) deben ser locales en la máquina desde la que se realiza la llamada. Un nombre de archivo puede ser un nombre UNC siempre que el nombre UNC sea el equipo local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterDriverExW** (Unicode) y **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**Información del controlador \_ \_ 2**](driver-info-2.md)
</dt> <dt>

[**Información del controlador \_ \_ 3**](driver-info-3.md)
</dt> <dt>

[**Información del controlador \_ \_ 4**](driver-info-4.md)
</dt> <dt>

[**Información del controlador \_ \_ 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

