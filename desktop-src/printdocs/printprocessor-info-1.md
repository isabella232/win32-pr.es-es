---
description: La \_ estructura PRINTPROCESSOR info \_ 1 especifica el nombre de un procesador de impresión instalado.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: Estructura de PRINTPROCESSOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697496"
---
# <a name="printprocessor_info_1-structure"></a>PRINTPROCESSOR \_ estructura de información \_ 1

La estructura **PRINTPROCESSOR \_ info \_ 1** especifica el nombre de un procesador de impresión instalado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de un procesador de impresión instalado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTPROCESSOR \_ info \_ 1W** (Unicode) y **\_ PRINTPROCESSOR \_ info \_ 1A** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




