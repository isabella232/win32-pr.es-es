---
description: La estructura PRINTER ENUM VALUES especifica el nombre del valor, el tipo y los datos de un valor de configuración de impresora devuelto por la \_ \_ función EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: PRINTER_ENUM_VALUES estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_ENUM_VALUES
- _PRINTER_ENUM_VALUESA
- _PRINTER_ENUM_VALUESW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a2b6fd8e548353dbede634d7b3bbaa08023d5e7bc2c8bc4cefbe37f7aba494ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470582"
---
# <a name="printer_enum_values-structure"></a>Estructura PRINTER \_ ENUM \_ VALUES

La **estructura PRINTER \_ ENUM \_ VALUES** especifica el nombre del valor, el tipo y los datos de un valor de configuración de impresora devuelto por la [**función EnumPrinterDataEx.**](enumprinterdataex.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_ENUM_VALUES {
  LPTSTR pValueName;
  DWORD  cbValueName;
  DWORD  dwType;
  LPBYTE pData;
  DWORD  cbData;
} PRINTER_ENUM_VALUES, *PPRINTER_ENUM_VALUES;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pValueName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del valor recuperado.

</dd> <dt>

**cbValueName**
</dt> <dd>

Número de bytes del miembro **pValueName,** incluido el carácter NULL de terminación.

</dd> <dt>

**dwType**
</dt> <dd>

Código que indica el tipo de datos a los que apunta el **miembro pData.** Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Puntero a un búfer que contiene los datos del valor recuperado.

</dd> <dt>

**cbData**
</dt> <dd>

Número de bytes recuperados en el **búfer pData.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTER \_ ENUM \_ VALUESW** (Unicode) e **\_ PRINTER \_ ENUM \_ VALUESA** (ANSI)<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

