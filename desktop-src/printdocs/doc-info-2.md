---
description: La estructura \_ DOC INFO \_ 2 describe un documento que se imprimirá.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: DOC_INFO_2 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 27d7753fa16abcfbc30b28bcc4343b2e1ef7996cad408b54fefb850feac9b17e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846265"
---
# <a name="doc_info_2-structure"></a>Estructura de DOC \_ INFO \_ 2

La **estructura DOC INFO \_ \_ 2** describe un documento que se imprimirá.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pDocName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre de un archivo de salida.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica el tipo de datos usados para registrar el documento.

</dd> <dt>

**dwMode**
</dt> <dd>

Informa al colador de impresión de la naturaleza de los datos que se deben seguir. Si este valor es cero, el administrador de trabajos de impresión trata los datos enviados por llamadas posteriores a [**WritePrinter**](writeprinter.md) como un trabajo de impresión normal (tanto si está en cola como si no depende de la propiedad de impresora). Si este valor es DI \_ CHANNEL, solo se abre un canal de comunicaciones. En este caso, los datos pasados a llamadas posteriores a **WritePrinter** se envían a la impresora o las llamadas posteriores a [**ReadPrinter**](readprinter.md) recuperan datos de la impresora. Este modo sigue siendo efectivo hasta que se llama a [**EndDoc.**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)

</dd> <dt>

**JobId**
</dt> <dd>

Reservado para uso interno; debe ser cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DOC \_ INFO \_ 2W** (Unicode) y **\_ DOC INFO \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




