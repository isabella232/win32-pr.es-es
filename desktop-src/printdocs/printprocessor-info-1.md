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
ms.openlocfilehash: 0aa94a2df1c44b53ec9fb8211f7eaed8c955f9f2c1cd824cd4634c754f8c337e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824745"
---
# <a name="printprocessor_info_1-structure"></a>PRINTPROCESSOR \_ INFO \_ 1 (estructura)

La **estructura PRINTPROCESSOR \_ INFO \_ 1** especifica el nombre de un procesador de impresión instalado.

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

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




