---
description: PRINTER \_ INFO \_ 6 especifica el valor de estado de una impresora.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: PRINTER_INFO_6 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 76255c563066ebcffde0fb2901426b186ec96504269842d286d2dc6ccca42ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947685"
---
# <a name="printer_info_6-structure"></a>Printer \_ INFO \_ 6 (estructura)

PRINTER **\_ INFO \_ 6** especifica el valor de estado de una impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwStatus**
</dt> <dd>

Estado de la impresora. Este miembro puede ser cualquier combinación razonable de los valores siguientes.



| Value                               | Significado                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| ESTADO DE \_ LA IMPRESORA \_ OCUPADO               | La impresora está ocupada.                                                                                          |
| PUERTA DE \_ ESTADO DE \_ IMPRESORA \_ ABIERTA         | La puerta de la impresora está abierta.                                                                                     |
| ERROR DE \_ ESTADO DE \_ LA IMPRESORA              | No se usa.                                                                                                     |
| INICIALIZACIÓN \_ DEL ESTADO DE LA \_ IMPRESORA       | La impresora se está inicializando.                                                                                  |
| ESTADO DE \_ LA \_ IMPRESORA \_ E/S ACTIVA         | La impresora está en un estado de entrada/salida activo.                                                                |
| FUENTE \_ MANUAL DE ESTADO DE LA \_ \_ IMPRESORA       | La impresora está en un estado de fuente manual.                                                                        |
| ESTADO \_ DE LA IMPRESORA SIN \_ \_ TONER          | Se ha agotado el tóner de la impresora.                                                                                  |
| ESTADO \_ DE LA IMPRESORA NO \_ \_ DISPONIBLE     | La impresora no está disponible para imprimir.                                                                    |
| ESTADO DE \_ LA IMPRESORA \_ SIN CONEXIÓN            | La impresora no está conectada.                                                                                       |
| ESTADO \_ DE LA IMPRESORA FUERA DE \_ \_ \_ MEMORIA    | La impresora se ha quedo sin memoria.                                                                            |
| BANDEJA DE \_ SALIDA DE ESTADO DE LA IMPRESORA \_ \_ \_ COMPLETA  | La bandeja de salida de la impresora está llena.                                                                             |
| PUNT DE \_ LA PÁGINA DE ESTADO DE LA \_ \_ IMPRESORA         | La impresora no puede imprimir la página actual.                                                                    |
| ATFILA \_ DE PAPEL DE ESTADO DE LA \_ \_ IMPRESORA         | El papel se afila en la impresora                                                                                |
| PAPEL DE \_ ESTADO \_ DE LA \_ IMPRESORA         | La impresora se ha quedado sin papel.                                                                                  |
| PROBLEMA DE \_ PAPEL DE ESTADO DE LA \_ \_ IMPRESORA     | La impresora tiene un problema de papel.                                                                              |
| ESTADO DE \_ LA \_ IMPRESORA EN PAUSA             | La impresora está en pausa.                                                                                        |
| ESTADO DE \_ LA IMPRESORA PENDIENTE DE \_ \_ ELIMINACIÓN  | La impresora está pendiente de eliminación como resultado de una llamada a la [**función DeletePrinter.**](deleteprinter.md) |
| GUARDADO \_ DE ENERGÍA DEL ESTADO DE LA \_ \_ IMPRESORA        | La impresora está en modo de ahorro de energía.                                                                            |
| IMPRESIÓN DE \_ ESTADO DE \_ IMPRESORA           | La impresora está imprimendo.                                                                                      |
| PROCESAMIENTO DEL \_ ESTADO DE \_ LA IMPRESORA         | La impresora está procesando un comando de la [**función SetPrinter.**](setprinter.md)                       |
| SERVIDOR DE \_ ESTADO DE \_ IMPRESORA \_ DESCONOCIDO    | El estado de la impresora es desconocido.                                                                                |
| TONER \_ DE ESTADO DE IMPRESORA \_ \_ BAJO         | La impresora tiene poca toner.                                                                                  |
| INTERVENCIÓN \_ DEL USUARIO DEL ESTADO DE LA \_ \_ IMPRESORA | La impresora tiene un error que requiere que el usuario haga algo.                                              |
| ESTADO DE \_ LA \_ IMPRESORA EN ESPERA            | La impresora está esperando.                                                                                       |
| ESTADO \_ DE LA IMPRESORA EN \_ \_ CALIENTE        | La impresora se está preparando.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ INFO \_ 6W** (Unicode) e **\_ PRINTER INFO \_ \_ 6A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 1**](printer-info-1.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 3**](printer-info-3.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 4**](printer-info-4.md)
</dt> <dt>

[**PRINTER \_ INFO \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




