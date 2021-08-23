---
description: La estructura PRINTER \_ INFO \_ 5 especifica información detallada de la impresora.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: PRINTER_INFO_5 estructura (Winspool.h)
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
ms.openlocfilehash: ef50f3bfd83a0c2dd49eb0a15cdae31f25588106926e606887292c705602dd44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731426"
---
# <a name="printer_info_5-structure"></a>Printer \_ INFO \_ 5 (estructura)

La **estructura PRINTER INFO \_ \_ 5** especifica información detallada de la impresora.

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

Puntero a una cadena terminada en NULL que especifica el nombre de la impresora.

</dd> <dt>

**pPortName**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica los puertos utilizados para transmitir datos a la impresora. Si una impresora está conectada a más de un puerto, los nombres de cada puerto deben estar separados por comas (por ejemplo, "LPT1:,LPT2:,LPT3:").

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
| ATRIBUTO \_ \_ DE IMPRESORA KEEPPRINTEDJOBS     | Si se establece, los trabajos se mantienen después de imprimirse. Si no se han eliminado, se eliminan los trabajos.                                                                                                               |
| ATRIBUTO \_ DE IMPRESORA \_ LOCAL               | La impresora es una impresora local.                                                                                                                                                             |
| RED DE \_ ATRIBUTOS DE \_ IMPRESORA             | La impresora es una conexión de impresora de red.                                                                                                                                                |
| ATRIBUTO \_ DE \_ IMPRESORA PUBLICADO           | Indica si la impresora está publicada en el servicio de directorio.                                                                                                                    |
| ATRIBUTO \_ DE IMPRESORA EN \_ COLA              | Si se establece, la impresora se pone en cola y se inicia la impresión después de que se pone en cola la última página. Si no se establece e PRINTER ATTRIBUTE DIRECT no está establecido, la impresora se cola e \_ imprime mientras se encuentra en \_ cola.      |
| SOLO SIN \_ FORMATO DE ATRIBUTO DE \_ \_ IMPRESORA           | Indica que solo se pueden colar trabajos de impresión de tipo de datos sin formato.                                                                                                                            |
| ATRIBUTO \_ DE IMPRESORA \_ COMPARTIDO              | La impresora se comparte.                                                                                                                                                                      |



 

En Windows XP y versiones posteriores de Windows, también se puede usar el siguiente valor.

| Valor                   | Significado                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FAX DE \_ ATRIBUTO DE \_ IMPRESORA | Si se establece, la impresora es una impresora de fax. [**AddPrinter**](addprinter.md)solo puede establecerlo, pero [**EnumPrinters**](enumprinters.md) y [**GetPrinter pueden recuperarlo.**](getprinter.md) |



 

En Windows Vista y versiones posteriores de Windows, también se pueden usar los siguientes valores.

| Valor                               | Significado                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| NOMBRE DESCRIPTIVO \_ DEL ATRIBUTO \_ DE \_ IMPRESORA  | Un equipo se ha conectado a esta impresora y le ha dado un nombre descriptivo.           |
| MÁQUINA DE \_ ATRIBUTOS DE \_ IMPRESORA         | La impresora es una conexión por máquina.                                             |
| USUARIO DE \_ INSERCIÓN \_ DE ATRIBUTO DE \_ IMPRESORA    | La impresora se instaló mediante la directiva de usuario Conexiones de impresora de inserción.     |
| MÁQUINA CON \_ INSERCIÓN \_ DE ATRIBUTOS DE \_ IMPRESORA | La impresora se instaló mediante la directiva de equipo Conexiones de impresora de inserción. |



 

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



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 5W** (Unicode) e **\_ PRINTER INFO \_ \_ 5A** (ANSI)<br/>                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 1**](printer-info-1.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 2**](printer-info-2.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 3**](printer-info-3.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 4**](printer-info-4.md)
</dt> </dl>

 

 




