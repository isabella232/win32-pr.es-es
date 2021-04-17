---
description: La estructura de la información de la impresora \_ \_ 5 especifica información detallada de la impresora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Estructura de PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720616"
---
# <a name="printer_info_5-structure"></a>Estructura de la información de la impresora \_ \_ 5

La estructura de la información de la **impresora \_ \_ 5** especifica información detallada de la impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pPrinterName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de la impresora.

</dd> <dt>

**pPortName**
</dt> <dd>

Puntero a una cadena terminada en null que identifica los puertos utilizados para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:, LPT2:, LPT3:").

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



 

</dd> <dt>

**DeviceNotSelectedTimeout**
</dt> <dd>

Este valor no se utiliza.

</dd> <dt>

**TransmissionRetryTimeout**
</dt> <dd>

Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 5W** (Unicode) e información de la **\_ impresora \_ \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 1**](printer-info-1.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**Información de la impresora \_ \_ 3**](printer-info-3.md)
</dt> <dt>

[**Información de la impresora \_ \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




