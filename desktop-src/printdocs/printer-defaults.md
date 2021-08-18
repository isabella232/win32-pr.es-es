---
description: La estructura PRINTER DEFAULTS especifica el tipo de datos predeterminado, el entorno, los datos de inicialización y los derechos de \_ acceso de una impresora.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: PRINTER_DEFAULTS estructura (Winspool.h)
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
ms.openlocfilehash: f1419948dddcd579e559ed084ce0af092cec373a7cd7f6d4b05d41f104f6666b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731693"
---
# <a name="printer_defaults-structure"></a>PRINTER \_ DEFAULTS (estructura)

La **estructura PRINTER \_ DEFAULTS** especifica el tipo de datos predeterminado, el entorno, los datos de inicialización y los derechos de acceso de una impresora.

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

Puntero a una cadena terminada en NULL que especifica el tipo de datos predeterminado para una impresora.

</dd> <dt>

**pDevMode**
</dt> <dd>

Puntero a una [**estructura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que identifica el entorno predeterminado y los datos de inicialización de una impresora.

</dd> <dt>

**DesiredAccess**
</dt> <dd>

Especifica los derechos de acceso deseados para una impresora. La [**función OpenPrinter**](openprinter.md) usa este miembro para establecer derechos de acceso a la impresora. Estos derechos pueden afectar al funcionamiento de las [**funciones SetPrinter**](setprinter.md) [**y DeletePrinter.**](deleteprinter.md) Los derechos de acceso pueden ser uno de los siguientes.



| Value                                       | Significado                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADMINISTRACIÓN DE \_ ACCESO A \_ IMPRESORAS                 | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md).                                                                                                 |
| USO DE \_ ACCESO A \_ IMPRESORAS                        | Para realizar operaciones de impresión básicas.                                                                                                                                                        |
| ADMINISTRACIÓN \_ LIMITADA DEL ACCESO A \_ \_ IMPRESORAS            | Para realizar tareas administrativas, como las proporcionadas por [**SetPrinter**](setprinter.md) y [**SetPrinterData**](setprinterdata.md). Este valor está disponible a partir de Windows 8.1. |
| ACCESO A \_ TODOS LOS \_ IMPRESORAS                        | Para realizar todas las tareas administrativas y las operaciones de impresión básicas excepto SYNCHRONIZE (vea [Derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights) ).                                   |
| valores de seguridad genéricos, como WRITE \_ DAC | Para permitir derechos de acceso de control específicos. Consulte [Derechos de acceso estándar.](/windows/desktop/SecAuthZ/standard-access-rights)                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ DEFAULTSW** (Unicode) e **\_ PRINTER \_ DEFAULTSA** (ANSI)<br/>                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

