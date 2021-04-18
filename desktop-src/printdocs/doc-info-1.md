---
description: La \_ estructura doc info \_ 1 describe un documento que se va a imprimir.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Estructura de DOC_INFO_1 (winspool. h)
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
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276666"
---
# <a name="doc_info_1-structure"></a>Estructura de información de documento \_ \_ 1

La estructura **doc \_ info \_ 1** describe un documento que se va a imprimir.

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

Puntero a una cadena terminada en null que especifica el nombre del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida. Para imprimir en una impresora, establezca este **valor en NULL**.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información de documento \_ \_ 1W** (Unicode) y **\_ información de documento \_ \_ 1A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

 




