---
description: La estructura de la información de la impresora \_ \_ 2 especifica información detallada de la impresora.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Estructura de PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546366"
---
# <a name="printer_info_2-structure"></a>Estructura de la información de la impresora \_ \_ 2

La estructura de la información de la **impresora \_ \_ 2** especifica información detallada de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pServerName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica el servidor que controla la impresora. Si esta cadena es **null**, la impresora se controla localmente.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de la impresora.

</dd> <dt>

**pShareName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica el punto de recurso compartido de la impresora. (Esta cadena solo se usa si la impresora \_ \_Se estableció una constante compartida de atributo para el miembro **attributes** .)

</dd> <dt>

**pPortName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica los puertos utilizados para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:, LPT2:, LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del controlador de impresora.

</dd> <dt>

**pComment**
</dt> <dd>

Un puntero a una cadena terminada en null que proporciona una breve descripción de la impresora.

</dd> <dt>

**pLocation**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica la ubicación física de la impresora (por ejemplo, "Bldg. 38, habitación 1164 ").

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados, como la orientación del papel y la resolución.

</dd> <dt>

**pSepFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del archivo que se usa para crear la página del separador. Esta página se utiliza para separar los trabajos de impresión que se envían a la impresora.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del procesador de impresión utilizado por la impresora. Puede usar la función [**EnumPrintProcessors**](enumprintprocessors.md) para obtener una lista de procesadores de impresión instalados en un servidor.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el tipo de datos utilizado para registrar el trabajo de impresión. Puede usar la función [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para obtener una lista de tipos de datos admitidos por un procesador de impresión específico.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntero a una cadena terminada en null que especifica los parámetros predeterminados del procesador de impresión.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para la impresora. Este miembro puede ser **null**.

</dd> <dt>

**Atributos**
</dt> <dd>

Atributos de la impresora. Este miembro puede ser cualquier combinación razonable de los siguientes valores.

| Value                                   | Significado                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| atributo de impresora \_ \_ directo              | El trabajo se envía directamente a la impresora (no se pone en cola).                                                                                                                                |
| el atributo de impresora se \_ \_ \_ completa \_ primero | Si se establece set y Printer para la puesta en cola de impresión, los trabajos que hayan finalizado la cola de impresión estarán programados para imprimirse antes que los trabajos que no hayan completado la cola de impresión.                          |
| atributo de impresora- \_ \_ habilitar \_ DEVQ        | Si se establece, se llama a **DevQueryPrint** . **DevQueryPrint** puede producir un error si las configuraciones de documento e impresora no coinciden. Si se establece esta marca, se mantendrán los documentos no coincidentes en la cola. |
| atributo de impresora \_ \_ oculto              | Reservado.                                                                                                                                                                               |
| atributo de impresora \_ \_ KEEPPRINTEDJOBS     | Si se establece, los trabajos se mantienen una vez que se imprimen. Si no se anula, se eliminan los trabajos.                                                                                                               |
| atributo de impresora \_ \_ local               | La impresora es una impresora local.                                                                                                                                                             |
| \_red de atributos de impresora \_             | La impresora es una conexión de impresora de red.                                                                                                                                                |
| atributo de impresora \_ \_ publicado           | Indica si la impresora está publicada en el servicio de directorio.                                                                                                                    |
| atributo de impresora \_ \_ en cola              | Si se establece, la impresora se pone en cola y comienza la impresión después de que la última página se haya puesto en cola. Si no se establece y \_ \_ no se establece el atributo de impresora Direct, la impresora se pone en cola y se imprime durante la puesta en cola.      |
| atributo de impresora \_ \_ solo sin formato \_           | Indica que solo se pueden poner en cola los trabajos de impresión de tipo de datos sin procesar.                                                                                                                            |
| atributo de impresora \_ \_ compartido              | La impresora está compartida.                                                                                                                                                                      |



 

En Windows XP y versiones posteriores de Windows, también se puede usar el valor siguiente.

| Value                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_fax de atributo de impresora \_ | Si se establece, la impresora es una impresora de fax. Solo se puede establecer mediante [**AddPrinter (**](addprinter.md), pero puede ser recuperado por [**EnumPrinters**](enumprinters.md) y [**GetPrinter**](getprinter.md). |



 

En Windows Vista y versiones posteriores de Windows, también se pueden usar los valores siguientes.

| Value                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| \_ \_ nombre descriptivo del atributo de impresora \_  | Un equipo se ha conectado a esta impresora y se le ha dado un nombre descriptivo.           |
| \_máquina de atributos de impresora \_         | La impresora es una conexión por equipo.                                             |
| atributo de impresora \_ \_ Push \_ User    | La impresora se instaló mediante la Directiva de usuario de las conexiones de impresión de la impresora.     |
| el \_ atributo de impresora \_ insertó el \_ equipo | La impresora se instaló mediante la Directiva de equipo de las conexiones de impresión de extracción. |



 

En Windows Server 2003, también se puede usar el valor siguiente.

| Value                  | Significado                                                                 |
|------------------------|-------------------------------------------------------------------------|
| atributo de impresora \_ \_ TS | Indica que la impresora está conectada actualmente a través de un servidor de Terminal Server. |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

Valor de prioridad que el administrador de trabajos de impresión utiliza para enrutar los trabajos de impresión.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Valor de prioridad predeterminado asignado a cada trabajo de impresión.

</dd> <dt>

**StartTime**
</dt> <dd>

La primera hora en la que la impresora imprimirá un trabajo. Este valor se expresa como minutos transcurridos desde 12:00 AM GMT (hora del meridiano de Greenwich).

</dd> <dt>

**UntilTime**
</dt> <dd>

La hora más reciente a la que la impresora imprimirá un trabajo. Este valor se expresa como minutos transcurridos desde 12:00 AM GMT (hora del meridiano de Greenwich).

</dd> <dt>

**Estado**
</dt> <dd>

El estado de la impresora. Este miembro puede ser cualquier combinación razonable de los siguientes valores.



| Value                               | Significado                                                          |
|-------------------------------------|------------------------------------------------------------------|
| Estado de la impresora \_ \_ ocupado               | La impresora está ocupada.                                             |
| puerta de estado de la impresora \_ \_ \_ abierta         | La puerta de la impresora está abierta.                                        |
| \_error de estado de la impresora \_              | La impresora está en un estado de error.                                |
| Estado de la impresora \_ \_ inicializando       | La impresora se está inicializando.                                     |
| \_e/s de estado de impresora \_ \_ activa         | La impresora está en un estado de entrada/salida activo                   |
| \_ \_ alimentación manual de estado de la impresora \_       | La impresora está en un estado de alimentación manual.                           |
| Estado de la impresora \_ \_ sin \_ tóner          | Se ha agotado el tóner de la impresora.                                     |
| Estado de la impresora \_ \_ no \_ disponible     | La impresora no está disponible para imprimir.                       |
| Estado de la impresora \_ \_ sin conexión            | La impresora no está conectada.                                          |
| \_Estado de la impresora \_ sin \_ \_ memoria    | La impresora se ha quedado sin memoria.                               |
| bandeja de salida de estado de la impresora \_ \_ \_ \_ llena  | La bandeja de salida de la impresora está llena.                                |
| Página de estado de la impresora \_ \_ \_ aparcan         | La impresora no puede imprimir la página actual.                       |
| \_atasco de \_ papel del estado de la impresora \_         | El papel está atascado en la impresora                                   |
| \_papel del estado de la impresora \_ \_         | La impresora se ha quedado sin papel.                                     |
| \_problema de \_ papel del estado de la impresora \_     | La impresora tiene un problema de papel.                                 |
| Estado de la impresora en \_ \_ pausa             | La impresora está en pausa.                                           |
| Estado de la impresora \_ \_ pendiente de \_ eliminación  | La impresora se está eliminando.                                    |
| Estado de la impresora- \_ \_ \_ guardar energía        | La impresora está en modo de ahorro de energía.                               |
| \_impresión del estado de la impresora \_           | La impresora se está imprimiendo.                                         |
| \_procesamiento del estado de la impresora \_         | La impresora está procesando un trabajo de impresión.                           |
| servidor de estado de impresora \_ \_ \_ desconocido    | No se conoce el estado de la impresora.                                   |
| Estado de la impresora \_ \_ tóner \_ bajo         | La impresora tiene poco tóner.                                     |
| Estado de la impresora- \_ \_ intervención del usuario \_ | La impresora tiene un error que requiere que el usuario haga algo. |
| Estado de la impresora en \_ \_ espera            | La impresora está en espera.                                          |
| \_preparación del \_ estado \_ de la impresora        | La impresora se está preparando.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

El número de trabajos de impresión que se han puesto en cola para la impresora.

</dd> <dt>

**AveragePPM**
</dt> <dd>

Número medio de páginas por minuto que se han impreso en la impresora.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 2W** (Unicode) y la información de la **\_ impresora \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> <dt>

[**descriptor de seguridad \_**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

