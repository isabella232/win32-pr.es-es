---
description: La estructura de MXDC de los \_ recursos S0PAGE de la \_ estructura t \_ \_ es una \_ \_ estructura de encabezado de escape MXDC que se \_ concatena con una \_ estructura de recurso t de MXDC XPS \_ S0PAGE \_ \_ .
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: MXDC_S0PAGE_RESOURCE_ESCAPE_T estructura (Mxdc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276776"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a>\_ \_ \_ Estructura T de recurso MXDC S0PAGE \_

La estructura de MXDC de los **\_ \_ recursos S0PAGE \_ \_** de la estructura t es una estructura de [**encabezado de escape MXDC que se concatena \_ \_ \_**](mxdcescapeheader.md) con una estructura de [**\_ \_ \_ recurso \_ t de MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**mxdcEscape**
</dt> <dd>

Una estructura de [**\_ encabezado de escape MXDC \_ \_ T**](mxdcescapeheader.md) con su miembro **opCode** establecida en MXDCOP \_ set \_ S0PAGE \_ Resource.

</dd> <dt>

**xpsS0PageResourcePassthrough**
</dt> <dd>

Una estructura [**MXDC \_ XPS \_ S0PAGE \_ Resource \_ T**](mxdcxpss0pageresource.md) que representa un recurso, como un archivo de fuente o de imagen, en una página de documento XPS.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se pasa en el parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama a esa función con el escape de [**\_ escape MXDC**](mxdc-escape.md) , y el miembro **opCode** de la estructura MXDC de [**encabezado de \_ escape \_ \_ T**](mxdcescapeheader.md) es **MXDCOP \_ set \_ S0PAGE \_ Resource**. El resultado es un recurso de página que se envía a MXDC.

Asigne memoria para el escape como se muestra a continuación, establezca los campos según sea necesario y, a continuación, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); sin embargo, puede haber más de una de estas llamadas entre las llamadas a **StartPage** y **EndPage**.

El consumo de transmisión por secuencias es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el **código de operación** **MXDCOP \_ set \_ S0PAGE \_** para cada recurso de la página antes de llamar a **ExtEscape** con el **código de operación** MXDCOP **\_ set \_ S0PAGE**.  

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

 

