---
description: La estructura \_ DOC INFO \_ 1 describe un documento que se imprimirá.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: DOC_INFO_1 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: f534031da1c8f8f50309d4a2db0bfa39fe272ac34f59d1b490c24026d8fee261
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950005"
---
# <a name="doc_info_1-structure"></a>Estructura \_ DE DOC INFO \_ 1

La **estructura DOC INFO \_ \_ 1** describe un documento que se imprimirá.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDocName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de un archivo de salida. Para imprimir en una impresora, establezca esta opción en **NULL.**

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica el tipo de datos usados para registrar el documento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DOC \_ INFO \_ 1W** (Unicode) e **\_ DOC INFO \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




