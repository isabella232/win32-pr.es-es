---
description: La estructura MXDC S0PAGE PASSTHROUGH ESCAPE T es una estructura MXDC ESCAPE HEADER T concatenada con una estructura \_ \_ \_ \_ \_ \_ \_ \_ MXDC S0PAGE \_ DATA \_ T.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: f8e0a46766f38aec16758a1efc9c0cbc775c2131b1279dcc47f92ed41e77c0e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099059"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>Estructura DE ESCAPE DE PASO A \_ TRAVÉS DE PÁGINA S0PAGE \_ \_ \_ de MXDC

La **estructura MXDC \_ S0PAGE \_ PASSTHROUGH ESCAPE \_ \_ T** es una estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) concatenada con una estructura [**\_ MXDC S0PAGE \_ DATA \_ T.**](mxdcs0pagedata.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Estructura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) con su **miembro opCode** establecido en **MXDCOP \_ SET \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Estructura [**MxdcS0PageData**](mxdcs0pagedata.md) que representa una página XPS-document.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape ESCAPE de [**\_ MXDC**](mxdc-escape.md) y el **miembro opCode** de la estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ SET \_ S0PAGE**. El resultado es que el Convertidor de documentos XML de Microsoft (MXDC) pasa la página a la impresora sin procesarla.

Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

La aplicación que realiza la llamada es responsable de validar el XML de la página del documento XPS.

El consumo de streaming es más eficaz si llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ SET \_ S0PAGE**.

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

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

