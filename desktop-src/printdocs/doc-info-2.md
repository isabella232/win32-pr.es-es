---
description: La \_ estructura doc info \_ 2 describe un documento que se va a imprimir.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Estructura de DOC_INFO_2 (winspool. h)
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
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697514"
---
# <a name="doc_info_2-structure"></a>Estructura de DOC \_ info \_ 2

La estructura **doc \_ info \_ 2** describe un documento que se va a imprimir.

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

Puntero a una cadena terminada en null que especifica el nombre del documento.

</dd> <dt>

**pOutputFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de un archivo de salida.

</dd> <dt>

**pDatatype**
</dt> <dd>

Puntero a una cadena terminada en null que identifica el tipo de datos utilizado para registrar el documento.

</dd> <dt>

**dwMode**
</dt> <dd>

Informa al administrador de trabajos de impresión de la naturaleza de los datos que deben seguir. Si este valor es cero, el administrador de trabajos de impresión trata los datos enviados por las llamadas subsiguientes a [**WritePrinter**](writeprinter.md) como un trabajo de impresión normal (tanto si se ha puesto en cola como si no depende de la propiedad de impresora). Si este valor es DI \_ Channel, solo se abre un canal de comunicaciones. En este caso, los datos pasados a las llamadas subsiguientes a **WritePrinter** se envían a la impresora o las llamadas posteriores a [**ReadPrinter**](readprinter.md) recuperan datos de la impresora. Este modo se mantiene efectivo hasta que se llama a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .

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
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información de documento \_ \_ 2W** (Unicode) y **\_ información de documento \_ \_ 2A** (ANSI)<br/>                                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[**ReadPrinter**](readprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




