---
description: La función AddPrinter agrega una impresora a la lista de impresoras admitidas para un servidor especificado.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Función AddPrinter (Winspool.h)
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
ms.openlocfilehash: 6034c330da19f5982e9bbacbf75cc16f0a7d10dd65f9c8bded2efa5cbda70835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601145"
---
# <a name="addprinter-function"></a>Función AddPrinter

La **función AddPrinter** agrega una impresora a la lista de impresoras admitidas para un servidor especificado.

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

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que se debe instalar la impresora. Si esta cadena es **NULL,** la impresora se instala localmente.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pPrinter.* Este valor debe ser 2.

</dd> <dt>

*pPrinter* \[ En\]
</dt> <dd>

Puntero a una [**estructura PRINTER \_ INFO \_ 2**](printer-info-2.md) que contiene información sobre la impresora. Debe especificar valores distintos de **NULL** para los miembros **pPrinterName**, **pPortName**, **pDriverName** y **pPrintProcessor** de esta estructura antes de llamar a **AddPrinter**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador (no seguro para subprocesos) para un nuevo objeto de impresora. Cuando haya terminado con el identificador, pásallo a la [**función ClosePrinter**](closeprinter.md) para cerrarlo.

Si se produce un error en la función, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

No llame a este método en [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El autor de la llamada debe [tener SeLoadDriverPrivilege.](/windows/desktop/SecAuthZ/authorization-constants)

El identificador devuelto no es seguro para subprocesos. Si los autores de la llamada necesitan usarlo simultáneamente en varios subprocesos, deben proporcionar acceso de sincronización personalizado al identificador de impresora mediante las [funciones de sincronización](/windows/desktop/Sync/synchronization-functions). Para evitar escribir código personalizado, la aplicación puede abrir un identificador de impresora en cada subproceso, según sea necesario.

Estos son los miembros de la estructura [**PRINTER \_ INFO \_ 2**](printer-info-2.md) que se pueden establecer antes de llamar a **la función AddPrinter:**

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

Los **miembros Status**, **cJobs** y **AveragePPM** de la estructura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) están reservados para su uso por la [**función GetPrinter.**](getprinter.md) No se deben establecer antes de llamar **a AddPrinter.**

Si **pSecurityDescriptor** es **NULL,** el sistema asigna un descriptor de seguridad predeterminado a la impresora. El descriptor de seguridad predeterminado tiene los permisos siguientes.



| Value                          | Descripción                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administradores y usuarios avanzados | Control total en la cola de impresión. Esto significa que los miembros de estos grupos pueden imprimir, administrar la cola (puede eliminar la cola, cambiar cualquier configuración de la cola, incluido el descriptor de seguridad) y administrar los trabajos de impresión de todos los usuarios (eliminar, pausar, reanudar, reiniciar trabajos). Tenga en cuenta que los usuarios avanzados no existen antes de Windows XP Professional.<br/> |
| Creador/propietario                  | Puede administrar trabajos propios. Esto significa que el usuario que envía trabajos puede administrar (eliminar, pausar, reanudar, reiniciar) sus propios trabajos.                                                                                                                                                                                                                                  |
| Todos.                       | Ejecutar y el control de lectura estándar. Esto significa que los miembros del grupo todos pueden imprimir y leer las propiedades de la cola de impresión.                                                                                                                                                                                                                     |



 

Una vez que una aplicación crea un objeto de impresora con la función **AddPrinter,** debe usar la [**función PrinterProperties**](printerproperties.md) para especificar la configuración correcta para el controlador de impresora asociado al objeto de impresora.

La **función AddPrinter** devuelve un error si ya existe un objeto de impresora con el mismo nombre, a menos que ese objeto esté marcado como pendiente de eliminación. En ese caso, no se elimina la impresora existente y los parámetros de creación de **AddPrinter** se usan para cambiar la configuración de impresora existente (como si la aplicación hubiera usado la [**función SetPrinter).**](setprinter.md)

Use la [**función EnumPrintProcessors**](enumprintprocessors.md) para enumerar el conjunto de procesadores de impresión instalados en un servidor. Use la [**función EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para enumerar el conjunto de tipos de datos que admite un procesador de impresión. Use la [**función EnumPorts**](enumports.md) para enumerar el conjunto de puertos disponibles. Use la [**función EnumPrinterDrivers para**](enumprinterdrivers.md) enumerar los controladores de impresora instalados.

El autor de la llamada **de la función AddPrinter** debe tener acceso SERVER ACCESS ADMINISTER al servidor en el que se va \_ a crear la \_ impresora. El identificador devuelto por la función tendrá el permiso PRINTER ALL ACCESS y se puede usar \_ para realizar operaciones administrativas en la \_ impresora.

Si se **pasa a la función DrvPrinterEvent** la marca de interfaz de usuario PRINTER EVENT FLAG NO, el controlador no debe usar una llamada de interfaz de usuario durante \_ \_ \_ \_ **DrvPrinterEvent**. Para realizar trabajos relacionados con la interfaz de usuario, el instalador debe usar la entrada **VendorSetup** en el archivo .inf de la impresora o, en el caso de los dispositivos Plug and Play, el instalador puede usar un coins instalador específico del dispositivo. Para obtener más información sobre **VendorSetup,** vea Microsoft Windows Driver Development Kit (DDK).

El Firewall de conexión a Internet (ICF) bloquea los puertos de impresora de forma predeterminada, pero se habilita una excepción para el uso compartido de archivos e impresión al **ejecutar AddPrinter**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
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

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

