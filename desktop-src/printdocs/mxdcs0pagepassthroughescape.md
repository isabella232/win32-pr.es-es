---
description: La \_ estructura MXDC S0PAGE \_ PASSTHROUGH \_ escape \_ t es una \_ estructura de encabezado de escape MXDC que se \_ \_ concatena con una estructura MXDC \_ S0PAGE \_ Data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T estructura (Mxdc. h)
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
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360896"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a>MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ T Structure

La estructura **MXDC \_ S0PAGE \_ PASSTHROUGH \_ escape \_ t** es una estructura de [**\_ \_ encabezado \_ de escape MXDC**](mxdcescapeheader.md) que se concatena con una estructura [**MXDC \_ S0PAGE \_ Data \_ t**](mxdcs0pagedata.md) .

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

Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en **MXDCOP \_ set \_ S0PAGE**.

</dd> <dt>

**xpsS0PageData**
</dt> <dd>

Una estructura [**MxdcS0PageData**](mxdcs0pagedata.md) que representa una página de documento XPS.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se pasa en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape [**de \_ escape MXDC**](mxdc-escape.md) y el miembro **opCode** de la estructura [**MXDC de encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ set \_ S0PAGE**. El resultado es que el convertidor de documentos XML de Microsoft (MXDC) pasa la página a la impresora sin procesarla.

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

El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ set \_ S0PAGE**.

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

 

