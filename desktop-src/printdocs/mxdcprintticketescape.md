---
description: La estructura MXDC PRINTTICKET ESCAPE T es una estructura \_ \_ \_ MXDC ESCAPE HEADER T concatenada con una estructura \_ \_ \_ \_ MXDC PRINTTICKET \_ DATA \_ T.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: eca1858bbbf09d4e3c3af8a91f9bb91550eddfd703f59e86112e65c56a43d553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099069"
---
# <a name="mxdc_printticket_escape_t-structure"></a>Estructura ESCAPE T de MXDC \_ PRINTTICKET \_ \_

La **estructura MXDC \_ PRINTTICKET ESCAPE \_ \_ T** es una estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**\_ MXDC PRINTTICKET \_ DATA \_ T.**](mxdcprintticketpassthrough.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Estructura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecido en MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE, MXDCOP PRINTTICKET FIXED DOC o \_ \_ \_ MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ.

</dd> <dt>

**printTicketData**
</dt> <dd>

Estructura [**MXDC \_ PRINTTICKET \_ DATA \_ T**](mxdcprintticketpassthrough.md) que contiene el vale de impresión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama a esa función con el escape [**ESCAPE \_ de MXDC**](mxdc-escape.md) y el miembro **opCode** de la estructura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE**, **MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ o** **MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ.** El resultado es escribir el vale de impresión en el archivo de documento XPS.

Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



Si **opCode** se establece en **MXDCOP \_ PRINTTICKET \_ FIXED \_ PAGE**, la llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Si **opCode** se establece en **MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC** o **MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ**, la llamada a **ExtEscape** debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

