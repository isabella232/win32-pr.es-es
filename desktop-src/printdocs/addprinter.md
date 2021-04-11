---
description: La función AddPrinter (agrega una impresora a la lista de impresoras admitidas para un servidor especificado.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Función AddPrinter ((winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276672"
---
# <a name="addprinter-function"></a>AddPrinter (función)

La función **AddPrinter (** agrega una impresora a la lista de impresoras admitidas para un servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del servidor en el que se debe instalar la impresora. Si esta cadena es **null**, la impresora se instala localmente.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Versión de la estructura a la que apunta *pPrinter* . Este valor debe ser 2.

</dd> <dt>

*pPrinter* \[ de\]
</dt> <dd>

Puntero a una estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que contiene información sobre la impresora. Debe especificar valores no **null** para los miembros **pPrinterName**, **pPortName**, **pDriverName** y **pPrintProcessor** de esta estructura antes de llamar a **AddPrinter (**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un identificador (no seguro para subprocesos) a un nuevo objeto Printer. Cuando haya terminado con el identificador, páselo a la función [**ClosePrinter**](closeprinter.md) para cerrarlo.

Si se produce un error en la función, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El autor de la llamada debe tener [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

El identificador devuelto no es seguro para subprocesos. Si los autores de las llamadas necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de la impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions). Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.

A continuación se muestran los miembros de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) que se pueden establecer antes de que se llame a la función **AddPrinter (** :

-   **Atributos**
-   **pPrintProcessor**
-   **DefaultPriority**
-   **Prioridad**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

Los miembros **status**, **cJobs** y **AveragePPM** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) están reservados para su uso por parte de la función [**GetPrinter**](getprinter.md) . No se deben establecer antes de llamar a **AddPrinter (**.

Si **pSecurityDescriptor** es **null**, el sistema asigna un descriptor de seguridad predeterminado a la impresora. El descriptor de seguridad predeterminado tiene los permisos siguientes.



| Value                          | Descripción                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administradores y usuarios avanzados | Control total en la cola de impresión. Esto significa que los miembros de estos grupos pueden imprimir, administrar la cola (puede eliminar la cola, cambiar cualquier valor de la cola, incluido el descriptor de seguridad) y administrar los trabajos de impresión de todos los usuarios (eliminar, pausar, reanudar, reiniciar trabajos). Tenga en cuenta que los usuarios avanzados no existen antes de Windows XP Professional.<br/> |
| Creador/propietario                  | Puede administrar sus propios trabajos. Esto significa que el usuario que envía trabajos puede administrar (eliminar, pausar, reanudar o reiniciar) sus propios trabajos.                                                                                                                                                                                                                                  |
| Todos                       | Ejecutar y control de lectura estándar. Esto significa que los miembros del grupo todos pueden imprimir y leer las propiedades de la cola de impresión.                                                                                                                                                                                                                     |



 

Después de que una aplicación crea un objeto de impresora con la función **AddPrinter (** , debe utilizar la función [**PrinterProperties**](printerproperties.md) para especificar la configuración correcta para el controlador de impresora asociado al objeto Printer.

La función **AddPrinter (** devuelve un error si ya existe un objeto de impresora con el mismo nombre, a menos que ese objeto esté marcado como pendiente de eliminación. En ese caso, no se elimina la impresora existente y los parámetros de creación de **AddPrinter (** se usan para cambiar la configuración de impresora existente (como si la aplicación hubiera usado la función [**SetPrinter**](setprinter.md) ).

Utilice la función [**EnumPrintProcessors**](enumprintprocessors.md) para enumerar el conjunto de procesadores de impresión instalado en un servidor. Utilice la función [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para enumerar el conjunto de tipos de datos que admite un procesador de impresión. Utilice la función [**EnumPorts**](enumports.md) para enumerar el conjunto de puertos disponibles. Utilice la función [**EnumPrinterDrivers**](enumprinterdrivers.md) para enumerar los controladores de impresora instalados.

El autor de la llamada de la función **AddPrinter (** debe tener acceso al servidor \_ \_ para administrar el acceso al servidor en el que se va a crear la impresora. El identificador devuelto por la función tendrá \_ permiso de \_ acceso a toda la impresora y se puede usar para realizar operaciones administrativas en la impresora.

Si se pasa a la función **DrvPrinterEvent** la \_ marca de evento de impresora \_ \_ sin marca de \_ IU, el controlador no debe usar una llamada de interfaz de usuario durante **DrvPrinterEvent**. Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada **VendorSetup** en el archivo. inf de la impresora o, para Plug and Play dispositivos, el instalador puede usar un Coinstalador específico del dispositivo. Para obtener más información acerca de **VendorSetup**, vea el kit de desarrollo de controladores (DDK) de Microsoft Windows.

El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se habilita una excepción para el uso compartido de archivos e impresoras al ejecutar **AddPrinter (**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterW** (Unicode) y **AddPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

