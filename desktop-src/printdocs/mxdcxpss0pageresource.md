---
description: La estructura MXDC XPS S0PAGE RESOURCE T contiene información sobre un recurso, como una imagen o fuente, que está asociado a una página de documento XPS y se va a pasar al archivo de salida del Convertidor de documentos \_ \_ \_ \_ XPS de Microsoft (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: MXDC_XPS_S0PAGE_RESOURCE_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 21035a99b6237c481a5b7560f469086ef2960d655ba32582ed273edb48910ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971184"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a>Estructura T de \_ recursos de MXDC XPS \_ \_ S0PAGE \_

La estructura **MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T** contiene información sobre un recurso, como una imagen o fuente, que está asociado a una página de documento XPS y se va a pasar al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

El tamaño total de esta estructura y el recurso al que apunta.

</dd> <dt>

**dwResourceType**
</dt> <dd>

Valor de tipo [**MXDC \_ S0 \_ PAGE \_ ENUMS**](mxdcs0pageenums.md) que indica el tipo de recurso, como la imagen TIFF o la fuente TrueType.

</dd> <dt>

**szUri**
</dt> <dd>

URI del recurso. No puede tener más de 260 bytes.

</dd> <dt>

**dwDataSize**
</dt> <dd>

Tamaño del recurso en bytes.

</dd> <dt>

**bData**
</dt> <dd>

Los datos del recurso en una matriz de bytes con el tamaño 1 + el tamaño del recurso.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se anexa a una estructura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) (que tiene su **opCode** establecido en **MXDCOP \_ SET \_ S0PAGERESOURCE)** para crear una estructura DE ESCAPE T de recursos [**de \_ S0PAGE \_ \_ \_ de MXDC.**](mxdcs0pageresourceescape.md) A continuación, se pasa la estructura T **MXDC \_ S0PAGE \_ RESOURCE ESCAPE \_ \_ T** resultante en el parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) a la que se llama con el escape [**ESCAPE \_ de MXDC.**](mxdc-escape.md) El efecto es enviar el recurso al MXDC para la conversión y escribirlo en el archivo de salida.

La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); sin embargo, puede haber más de una llamada de este tipo entre las llamadas **a StartPage** y **EndPage**.

El consumo de streaming es más eficaz si llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el código de operación **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** **para** cada recurso de la página antes de llamar a **ExtEscape** con el **código** de operación **MXDCOP \_ SET \_ S0PAGE** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mxdc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

