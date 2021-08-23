---
description: La estructura PRINTER \_ INFO \_ 2 especifica información detallada de la impresora.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: PRINTER_INFO_2 estructura (Winspool.h)
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
ms.openlocfilehash: 1f7a2b871cc0181fbceab56e4ac14170bf46fa1b31081f4b4365ad7296ec2e85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600615"
---
# <a name="printer_info_2-structure"></a>Printer \_ INFO \_ 2 (estructura)

La **estructura PRINTER INFO \_ \_ 2** especifica información detallada de la impresora.

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

Puntero a una cadena terminada en NULL que identifica el servidor que controla la impresora. Si esta cadena es **NULL,** la impresora se controla localmente.

</dd> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora.

</dd> <dt>

**pShareName**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica el punto de recurso compartido de la impresora. (Esta cadena solo se usa si printer \_ Se \_ estableció la constante ATTRIBUTE SHARED para el **miembro Attributes).**

</dd> <dt>

**pPortName**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los puertos utilizados para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:,LPT2:,LPT3:").

</dd> <dt>

**pDriverName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador de impresora.

</dd> <dt>

**pComment**
</dt> <dd>

Puntero a una cadena terminada en NULL que proporciona una breve descripción de la impresora.

</dd> <dt>

**pLocation**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la ubicación física de la impresora (por ejemplo, "Bldg. 38, Habitación 1164").

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define los datos de impresora predeterminados, como la orientación del papel y la resolución.

</dd> <dt>

**pSepFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del archivo utilizado para crear la página separadora. Esta página se usa para separar los trabajos de impresión enviados a la impresora.

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del procesador de impresión utilizado por la impresora. Puede usar la función [**EnumPrintProcessors**](enumprintprocessors.md) para obtener una lista de procesadores de impresión instalados en un servidor.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el tipo de datos utilizado para registrar el trabajo de impresión. Puede usar la función [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para obtener una lista de tipos de datos admitidos por un procesador de impresión específico.

</dd> <dt>

**pParameters**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica los parámetros predeterminados del procesador de impresión.

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

Puntero a una estructura [**\_ DESCRIPTOR DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) para la impresora. Este miembro puede ser **NULL.**

</dd> <dt>

**Atributos**
</dt> <dd>

Atributos de impresora. Este miembro puede ser cualquier combinación razonable de los valores siguientes.

| Valor                                   | Significado                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATRIBUTO \_ DE \_ IMPRESORA DIRECTO              | El trabajo se envía directamente a la impresora (no está en cola).                                                                                                                                |
| EL \_ ATRIBUTO PRINTER SE COMPLETA \_ \_ \_ PRIMERO | Si set e printer se establecen para la cola de impresión, los trabajos que hayan completado la cola se programan para imprimirse antes que los trabajos que no hayan completado la cola.                          |
| ATRIBUTO \_ PRINTER \_ ENABLE \_ DEVQ        | Si se establece, **se llama a DevQueryPrint.** **DevQueryPrint puede producir** un error si las configuraciones de documentos e impresoras no coinciden. Al establecer esta marca, los documentos no coincidentes se mantienen en la cola. |
| ATRIBUTO DE \_ IMPRESORA \_ OCULTO              | Reservado.                                                                                                                                                                               |
| ATRIBUTO \_ \_ DE IMPRESORA KEEPPRINTEDJOBS     | Si se establece, los trabajos se mantienen después de imprimirse. Si no se han creado, se eliminan los trabajos.                                                                                                               |
| ATRIBUTO \_ DE IMPRESORA \_ LOCAL               | La impresora es una impresora local.                                                                                                                                                             |
| RED DE \_ ATRIBUTOS DE \_ IMPRESORA             | La impresora es una conexión de impresora de red.                                                                                                                                                |
| ATRIBUTO \_ DE \_ IMPRESORA PUBLICADO           | Indica si la impresora está publicada en el servicio de directorio.                                                                                                                    |
| ATRIBUTO \_ DE IMPRESORA EN \_ COLA              | Si se establece, la impresora se pone en cola y se inicia la impresión después de que se pone en cola la última página. Si no se establece e PRINTER ATTRIBUTE DIRECT no está establecido, la impresora se cola e \_ imprime mientras se encuentra en \_ cola.      |
| SOLO SIN \_ FORMATO DE ATRIBUTO DE \_ \_ IMPRESORA           | Indica que solo se pueden colar trabajos de impresión de tipo de datos sin procesar.                                                                                                                            |
| ATRIBUTO DE \_ IMPRESORA \_ COMPARTIDO              | La impresora se comparte.                                                                                                                                                                      |



 

En Windows XP y versiones posteriores de Windows, también se puede usar el siguiente valor.

| Valor                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FAX DE \_ ATRIBUTO DE \_ IMPRESORA | Si se establece, la impresora es una impresora de fax. [**AddPrinter**](addprinter.md)solo puede establecerlo, pero [**EnumPrinters**](enumprinters.md) y [**GetPrinter pueden recuperarlo.**](getprinter.md) |



 

En Windows Vista y versiones posteriores de Windows, también se pueden usar los siguientes valores.

| Value                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| NOMBRE DESCRIPTIVO \_ DEL ATRIBUTO \_ DE \_ IMPRESORA  | Un equipo se ha conectado a esta impresora y le ha dado un nombre descriptivo.           |
| MÁQUINA DE \_ ATRIBUTOS DE \_ IMPRESORA         | La impresora es una conexión por máquina.                                             |
| USUARIO \_ DE INSERCIÓN \_ DE ATRIBUTO DE \_ IMPRESORA    | La impresora se instaló mediante la directiva de usuario Insertar conexiones de impresora.     |
| MÁQUINA CON \_ INSERCIÓN \_ DE ATRIBUTOS DE \_ IMPRESORA | La impresora se instaló mediante la directiva de equipo Conexiones de impresora de inserción. |



 

En Windows Server 2003, también se puede usar el siguiente valor.

| Value                  | Significado                                                                 |
|------------------------|-------------------------------------------------------------------------|
| TS \_ DE \_ ATRIBUTO DE IMPRESORA | Indica que la impresora está conectada actualmente a través de un servidor terminal. |



 

</dd> <dt>

**Prioridad**
</dt> <dd>

Valor de prioridad que el colador usa para enrutar los trabajos de impresión.

</dd> <dt>

**DefaultPriority**
</dt> <dd>

Valor de prioridad predeterminado asignado a cada trabajo de impresión.

</dd> <dt>

**StartTime**
</dt> <dd>

La primera vez que la impresora imprimirá un trabajo. Este valor se expresa como minutos transcurridos desde las 12:00 a.m. GMT (hora media de Greenwich).

</dd> <dt>

**UntilTime**
</dt> <dd>

La hora más reciente a la que la impresora imprimirá un trabajo. Este valor se expresa como minutos transcurridos desde las 12:00 a.m. GMT (hora media de Greenwich).

</dd> <dt>

**Estado**
</dt> <dd>

Estado de la impresora. Este miembro puede ser cualquier combinación razonable de los valores siguientes.



| Valor                               | Significado                                                          |
|-------------------------------------|------------------------------------------------------------------|
| ESTADO DE \_ LA IMPRESORA \_ OCUPADO               | La impresora está ocupada.                                             |
| PUERTA DE \_ ESTADO DE LA IMPRESORA \_ \_ ABIERTA         | La puerta de la impresora está abierta.                                        |
| ERROR DE \_ ESTADO DE \_ LA IMPRESORA              | La impresora está en un estado de error.                                |
| INICIALIZACIÓN \_ DEL ESTADO DE LA \_ IMPRESORA       | La impresora se está inicializando.                                     |
| ESTADO DE \_ LA \_ IMPRESORA \_ E/S ACTIVA         | La impresora está en un estado de entrada/salida activo                   |
| FUENTE \_ MANUAL DE ESTADO DE LA \_ \_ IMPRESORA       | La impresora está en un estado de fuente manual.                           |
| ESTADO \_ DE LA IMPRESORA SIN \_ \_ TONER          | Se ha agotado el tóner de la impresora.                                     |
| ESTADO \_ DE LA IMPRESORA NO \_ \_ DISPONIBLE     | La impresora no está disponible para impresión.                       |
| ESTADO DE \_ LA IMPRESORA \_ SIN CONEXIÓN            | La impresora no está conectada.                                          |
| ESTADO DE \_ LA IMPRESORA FUERA DE \_ \_ \_ MEMORIA    | La impresora se ha quedo sin memoria.                               |
| BANDEJA DE \_ SALIDA DE ESTADO DE LA IMPRESORA \_ \_ \_ COMPLETA  | La bandeja de salida de la impresora está llena.                                |
| PUNT \_ DE LA PÁGINA DE ESTADO DE LA \_ \_ IMPRESORA         | La impresora no puede imprimir la página actual.                       |
| ATASCO \_ DE PAPEL DE ESTADO DE LA \_ \_ IMPRESORA         | El papel está atascado en la impresora                                   |
| PAPEL DE \_ ESTADO DE LA IMPRESORA \_ \_ FUERA         | La impresora se ha quedado sin papel.                                     |
| PROBLEMA DE \_ PAPEL DE ESTADO DE LA \_ \_ IMPRESORA     | La impresora tiene un problema de papel.                                 |
| ESTADO DE \_ LA \_ IMPRESORA EN PAUSA             | La impresora está en pausa.                                           |
| ESTADO DE \_ LA IMPRESORA PENDIENTE DE \_ \_ ELIMINACIÓN  | La impresora se está eliminando.                                    |
| GUARDADO \_ DE ENERGÍA DEL ESTADO DE LA \_ \_ IMPRESORA        | La impresora está en modo de ahorro de energía.                               |
| IMPRESIÓN DE \_ ESTADO DE \_ IMPRESORA           | La impresora está imprimiendo.                                         |
| PROCESAMIENTO DEL \_ ESTADO DE \_ LA IMPRESORA         | La impresora está procesando un trabajo de impresión.                           |
| SERVIDOR DE \_ ESTADO \_ DE IMPRESORA \_ DESCONOCIDO    | Se desconoce el estado de la impresora.                                   |
| EL ESTADO \_ DE LA IMPRESORA ES \_ \_ BAJO         | La impresora tiene poca toner.                                     |
| INTERVENCIÓN \_ DEL USUARIO DEL ESTADO DE LA \_ \_ IMPRESORA | La impresora tiene un error que requiere que el usuario haga algo. |
| ESTADO DE \_ LA \_ IMPRESORA EN ESPERA            | La impresora está esperando.                                          |
| ESTADO \_ DE LA IMPRESORA EN \_ \_ CALIENTE        | La impresora se está preparando.                                       |



 

</dd> <dt>

**cJobs**
</dt> <dd>

Número de trabajos de impresión que se han puesto en cola para la impresora.

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
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 2W** (Unicode) e **\_ PRINTER INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> <dt>

[**DESCRIPTOR \_ DE SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

