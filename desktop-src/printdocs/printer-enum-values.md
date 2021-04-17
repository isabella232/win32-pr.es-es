---
description: La \_ estructura de valores enum de impresora \_ especifica el nombre del valor, el tipo y los datos para un valor de configuración de impresora devuelto por la función EnumPrinterDataEx.
ms.assetid: 87eb1452-0d9d-46bd-8af8-0542a11a929b
title: Estructura de PRINTER_ENUM_VALUES (winspool. h)
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
ms.openlocfilehash: ea73318db7a91fa4d422624b1c3c0c6f09d97cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716336"
---
# <a name="printer_enum_values-structure"></a>\_Estructura de valores de enumeración de impresora \_

La estructura de **\_ \_ valores enum de impresora** especifica el nombre del valor, el tipo y los datos para un valor de configuración de impresora devuelto por la función [**EnumPrinterDataEx**](enumprinterdataex.md) .

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

Puntero a una cadena terminada en null que especifica el nombre del valor recuperado.

</dd> <dt>

**cbValueName**
</dt> <dd>

El número de bytes en el miembro **pValueName** , incluido el carácter nulo de terminación.

</dd> <dt>

**dwType**
</dt> <dd>

Código que indica el tipo de datos al que apunta el miembro **pdata** . Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

**pData**
</dt> <dd>

Puntero a un búfer que contiene los datos para el valor recuperado.

</dd> <dt>

**cbData**
</dt> <dd>

Número de bytes recuperados en el búfer de **pdata** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ \_ Enumeración \_ de impresora VALUESW** (Unicode) y **\_ \_ \_ valores de enumeración de impresora** (ANSI)<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> </dl>

 

