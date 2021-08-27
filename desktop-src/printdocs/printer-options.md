---
description: Representa las opciones de impresora.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: PRINTER_OPTIONS estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d7eb7be8443c6a49c670e0573a79831a7aacfd88087f6ab19de632223b8588c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091755"
---
# <a name="printer_options-structure"></a>PRINTER \_ OPTIONS (estructura)

Representa las opciones de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura **OPCIONES \_ DE IMPRESORA.**

</dd> <dt>

**dwFlags**
</dt> <dd>

Conjunto de [**MARCAS DE OPCIÓN \_ \_ DE**](printer-option-flags.md) IMPRESORA que especifica cómo otras funciones usarán el identificador de una impresora devuelta por [**OpenPrinter2.**](openprinter2.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**OpenPrinter2**](openprinter2.md)
</dt> <dt>

[**MARCAS DE \_ OPCIÓN \_ DE IMPRESORA**](printer-option-flags.md)
</dt> </dl>

 

 




