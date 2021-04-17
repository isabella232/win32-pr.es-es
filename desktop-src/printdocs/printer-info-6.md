---
description: La \_ información de la impresora \_ 6 especifica el valor de estado de una impresora.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Estructura de PRINTER_INFO_6 (winspool. h)
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
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716945"
---
# <a name="printer_info_6-structure"></a>Estructura de la información de la impresora \_ \_ 6

La **información de la impresora \_ \_ 6** especifica el valor de estado de una impresora.

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

El estado de la impresora. Este miembro puede ser cualquier combinación razonable de los siguientes valores.



| Value                               | Significado                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Estado de la impresora \_ \_ ocupado               | La impresora está ocupada.                                                                                          |
| puerta de estado de la impresora \_ \_ \_ abierta         | La puerta de la impresora está abierta.                                                                                     |
| \_error de estado de la impresora \_              | No se utiliza.                                                                                                     |
| Estado de la impresora \_ \_ inicializando       | La impresora se está inicializando.                                                                                  |
| \_e/s de estado de impresora \_ \_ activa         | La impresora está en un estado de entrada/salida activo                                                                |
| \_ \_ alimentación manual de estado de la impresora \_       | La impresora está en un estado de alimentación manual.                                                                        |
| Estado de la impresora \_ \_ sin \_ tóner          | Se ha agotado el tóner de la impresora.                                                                                  |
| Estado de la impresora \_ \_ no \_ disponible     | La impresora no está disponible para imprimir.                                                                    |
| Estado de la impresora \_ \_ sin conexión            | La impresora no está conectada.                                                                                       |
| \_Estado de la impresora \_ sin \_ \_ memoria    | La impresora se ha quedado sin memoria.                                                                            |
| bandeja de salida de estado de la impresora \_ \_ \_ \_ llena  | La bandeja de salida de la impresora está llena.                                                                             |
| Página de estado de la impresora \_ \_ \_ aparcan         | La impresora no puede imprimir la página actual.                                                                    |
| \_atasco de \_ papel del estado de la impresora \_         | El papel está atascado en la impresora                                                                                |
| \_papel del estado de la impresora \_ \_         | La impresora se ha quedado sin papel.                                                                                  |
| \_problema de \_ papel del estado de la impresora \_     | La impresora tiene un problema de papel.                                                                              |
| Estado de la impresora en \_ \_ pausa             | La impresora está en pausa.                                                                                        |
| Estado de la impresora \_ \_ pendiente de \_ eliminación  | La impresora está pendiente de eliminación como resultado de una llamada a la función [**DeletePrinter**](deleteprinter.md) . |
| Estado de la impresora- \_ \_ \_ guardar energía        | La impresora está en modo de ahorro de energía.                                                                            |
| \_impresión del estado de la impresora \_           | La impresora se está imprimiendo.                                                                                      |
| \_procesamiento del estado de la impresora \_         | La impresora está procesando un comando de la función [**SetPrinter**](setprinter.md) .                       |
| servidor de estado de impresora \_ \_ \_ desconocido    | No se conoce el estado de la impresora.                                                                                |
| Estado de la impresora \_ \_ tóner \_ bajo         | La impresora tiene poco tóner.                                                                                  |
| Estado de la impresora- \_ \_ intervención del usuario \_ | La impresora tiene un error que requiere que el usuario haga algo.                                              |
| Estado de la impresora en \_ \_ espera            | La impresora está en espera.                                                                                       |
| \_preparación del \_ estado \_ de la impresora        | La impresora se está preparando.                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | Información de la **\_ impresora \_ \_ 6W** (Unicode) y la información de la **\_ impresora \_ \_ 6A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
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
</dt> <dt>

[**Información de la impresora \_ \_ 5**](printer-info-5.md)
</dt> </dl>

 

 




