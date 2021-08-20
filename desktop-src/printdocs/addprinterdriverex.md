---
description: La función AddPrinterDriverEx instala un controlador de impresora local o remoto y vincula los archivos de configuración, datos y controladores.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Función AddPrinterDriverEx (Winspool.h)
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
ms.openlocfilehash: 00bd65ad415a97bbab825e4a13c8ad985d1d7f9b79d7b46e3f8f7ea6b5e5f0dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868814"
---
# <a name="addprinterdriverex-function"></a>Función AddPrinterDriverEx

La **función AddPrinterDriverEx** instala un controlador de impresora local o remoto y vincula los archivos de configuración, datos y controladores. Además de tener las funcionalidades de [**AddPrinterDriver,**](addprinterdriver.md)también tiene opciones que permiten una actualización estricta, una degradación estricta, la copia solo de archivos más recientes y la copia de todos los archivos (independientemente de las marcas de tiempo de archivo).

> [!Note]  
> Ya no se recomienda instalar un controlador de impresora sin un paquete de controladores. En [**su lugar, use InstallPrinterDriverFromPackage.**](installprinterdriverfrompackage.md)

 

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

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que se debe instalar el controlador. Si este parámetro es **NULL,** la función instala el controlador en el equipo local.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pDriverInfo.* Este valor puede ser 2, 3, 4, 6 u 8.

</dd> <dt>

*pDriverInfo* \[ in, out\]
</dt> <dd>

Puntero a una estructura que contiene información del controlador de impresora. Puede ser uno de los siguientes.



| Valor de Level                                                                                       | DRIVER \_ INFO \_ \* (estructura)                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 2**](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 3**](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 4**](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 6**](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <dt>**8**</dt> </dl> | [**INFORMACIÓN \_ DEL CONTROLADOR \_ 8**](driver-info-8.md)<br/> |



 

Si el **miembro pEnvironment** de la estructura a la que apunta *pDriverInfo* es **NULL,** la función usa el entorno actual del llamador o cliente, no el entorno del destino o servidor.

</dd> <dt>

*dwFileCopyFlags* \[ En\]
</dt> <dd>

Opciones para copiar los archivos del controlador. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <dt>**COPIA DE \_ TODOS \_ LOS ARCHIVOS DE APD \_**</dt> </dl>                | Agregue el controlador de impresora y copie todos los archivos del directorio printer-driver. Las marcas de tiempo de archivo se omiten con esta opción.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <dt>**COPIA DE APD \_ \_ DESDE EL \_ DIRECTORIO**</dt> </dl> | Agregue el controlador de impresora con los nombres de archivo completos especificados en la [**estructura \_ DRIVER INFO \_ 6.**](driver-info-6.md) Esta marca es ORed junto con una de las otras marcas de copia. Si se establece esta marca, se producirá un error en **AddPrinterDriverEx** si los archivos no existen donde se especifica que existan mediante la estructura **DRIVER INFO \_ \_ 6.** No es necesario copiar los archivos en el directorio del controlador de impresora del sistema. Consulte los comentarios.<br/> **Windows 2000:** Esta marca no se admite.<br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <dt>**COPIA DE \_ ARCHIVOS \_ NUEVOS DE \_ APD**</dt> </dl>                | Agregue el controlador de impresora y copie los archivos del directorio printer-driver que son más recientes que los archivos correspondientes que están actualmente en uso. Esta marca emula el comportamiento de [**AddPrinterDriver.**](addprinterdriver.md)<br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <dt>**DEGRADACIÓN \_ ESTRICTA DE APD \_**</dt> </dl>           | Agregue el controlador de impresora solo si todos los archivos del directorio printer-driver son anteriores a los archivos correspondientes actualmente en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <dt>**ACTUALIZACIÓN ESTRICTA DE APD \_ \_**</dt> </dl>                 | Agregue el controlador de impresora solo si todos los archivos del directorio printer-driver son más recientes que los archivos correspondientes actualmente en uso.<br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

Si se sabe que el controlador de impresora tiene problemas para trabajar con el sistema operativo, **AddPrinterDriverEx** producirá uno de los siguientes códigos de error:



| Código de error                      | Significado                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR CONTROLADOR \_ DE \_ IMPRESORA \_ BLOQUEADO | El controlador no funciona en el sistema operativo.                                                                                                         |
| ERROR \_ EL CONTROLADOR DE IMPRESORA HA SIDO \_ \_ AMONESTÓ  | El controlador no es confiable en el sistema operativo. Sin embargo, si se especifica APD \_ INSTALL \_ WARNED DRIVER, el controlador se instala y no se muestra \_ ninguna advertencia. |



 

Para obtener más información, vea la sección Notas.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El autor de la llamada debe [tener SeLoadDriverPrivilege.](/windows/desktop/SecAuthZ/authorization-constants)

Antes de llamar **a la función AddPrinterDriverEx,** todos los archivos requeridos por el controlador deben copiarse en el directorio printer-driver del sistema. Para recuperar el nombre de este directorio, llame a la [**función GetPrinterDriverDirectory.**](getprinterdriverdirectory.md)

Para determinar qué controladores de impresora están instalados actualmente, llame a [**la función EnumPrinterDrivers.**](enumprinterdrivers.md)

Si el controlador de impresora se ha agregado correctamente, la función llama a la función DrvDriverEvent (DRIVER \_ EVENT \_ INITIALIZE, Level, DRIVER \_ INFO , \_ \* lparam) para permitir que el controlador realice las inicializaciones necesarias durante la instalación de un controlador de impresora. Para obtener más información **sobre DrvDriverEvent,** vea Microsoft Windows Driver Development Kit (DDK)

El controlador no debe usar una llamada de interfaz de usuario durante la llamada a **DrvDriverEvent**. Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada VendorSetup en el archivo .inf de la impresora o, en el caso de los dispositivos Plug and Play, el instalador puede usar un coins instalador específico del dispositivo. Para obtener más información sobre VendorSetup, consulte el DDK.

Los archivos a los que se hace referencia en la [**estructura DRIVER \_ INFO \_ 6**](driver-info-6.md) deben ser locales en la máquina desde la que se realiza la llamada. Un nombre de archivo puede ser un nombre UNC siempre que el nombre UNC sea el equipo local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterDriverExW** (Unicode) y **AddPrinterDriverExA** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL CONTROLADOR \_ 2**](driver-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 3**](driver-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 4**](driver-info-4.md)
</dt> <dt>

[**INFORMACIÓN \_ DEL \_ CONTROLADOR 6**](driver-info-6.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

