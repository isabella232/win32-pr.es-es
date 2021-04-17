---
description: La \_ estructura valores predeterminados de impresora especifica el tipo de datos, el entorno, los datos de inicialización y los derechos de acceso predeterminados para una impresora.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Estructura de PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678043"
---
# <a name="printer_defaults-structure"></a>\_Estructura de valores predeterminados de impresora

La **estructura \_ valores predeterminados de impresora** especifica el tipo de datos, el entorno, los datos de inicialización y los derechos de acceso predeterminados para una impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el tipo de datos predeterminado para una impresora.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que identifica el entorno predeterminado y los datos de inicialización de una impresora.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Especifica los derechos de acceso deseados para una impresora. La función [**OpenPrinter**](openprinter.md) usa este miembro para establecer los derechos de acceso a la impresora. Estos derechos pueden afectar al funcionamiento de las funciones [**SetPrinter**](setprinter.md) y [**DeletePrinter**](deleteprinter.md) . Los derechos de acceso pueden ser uno de los siguientes.



| Value                                       | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administrar el acceso a las impresoras \_                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| \_uso de acceso a impresoras \_                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| \_acceso limitado de administración de acceso a impresoras \_ \_            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| \_todo el \_ acceso a la impresora                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto la sincronización (consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Impresora \_ DEFAULTSW** (Unicode) y **\_ \_ DEFAULTSA de impresora** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

