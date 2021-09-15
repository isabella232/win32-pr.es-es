---
description: La estructura PRINTPROCESSOR \_ INFO \_ 1 especifica el nombre de un procesador de impresión instalado.
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: PRINTPROCESSOR_INFO_1 estructura (Winspool.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359703"
---
# <a name="printprocessor_info_1-structure"></a>PRINTPROCESSOR \_ INFO \_ 1 (estructura)

La **estructura PRINTPROCESSOR \_ INFO \_ 1** especifica el nombre de un procesador de impresión instalado.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de un procesador de impresión instalado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ PRINTPROCESSOR \_ INFO \_ 1W** (Unicode) e **\_ PRINTPROCESSOR \_ INFO \_ 1A** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




