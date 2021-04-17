---
description: La \_ estructura de escape t de MXDC PrintTicket \_ \_ es una \_ estructura de encabezado de escape MXDC \_ \_ T concatenada con una \_ estructura MXDC PRINTTICKET \_ Data \_ t.
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: MXDC_PRINTTICKET_ESCAPE_T estructura (Mxdc. h)
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
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653029"
---
# <a name="mxdc_printticket_escape_t-structure"></a>\_ \_ \_ Estructura T de MXDC PRINTTICKET

La estructura de **\_ \_ escape \_ t de MXDC PrintTicket** es una estructura de [**encabezado de \_ escape MXDC \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**MXDC \_ PRINTTICKET \_ Data \_ t**](mxdcprintticketpassthrough.md) .

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

Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en MXDCOP \_ PrintTicket Fixed \_ \_ Page, MXDCOP \_ PrintTicket \_ fixed \_ doc o MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.

</dd> <dt>

**printTicketData**
</dt> <dd>

Una estructura de [**\_ \_ datos \_ de PRINTTICKET MXDC**](mxdcprintticketpassthrough.md) que contiene la solicitud de impresión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama a esa función con el escape de [**\_ escape MXDC**](mxdc-escape.md) y el miembro **opCode** de la estructura MXDC de [**encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ \_ \_ Página fija de PrintTicket**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**. El resultado es escribir la solicitud de impresión en el archivo de documento XPS.

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



Si el **código de operación** se establece en la **\_ \_ \_ Página fija MXDCOP PRINTTICKET**, se debe realizar la llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage). Si el **código de operación** se establece en **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la llamada a **ExtEscape** debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mxdc. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**\_escape MXDC**](mxdc-escape.md)
</dt> </dl>

 

