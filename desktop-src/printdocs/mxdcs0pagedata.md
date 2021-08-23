---
description: La estructura MXDC S0PAGE DATA T contiene una página de documento XPS que se pasará al archivo de salida del Convertidor de documentos \_ \_ \_ XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: MXDC_S0PAGE_DATA_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 1ff54325859acef6da136c4bce20286bc7c746d8880d8994ca834213adf57b58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776555"
---
# <a name="mxdc_s0page_data_t-structure"></a>Estructura T \_ de DATOS S0PAGE \_ \_ de MXDC

La **estructura MXDC \_ S0PAGE \_ DATA \_ T** contiene una página de documento XPS que se pasará al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwSize**
</dt> <dd>

Tamaño del búfer de salida, **bData**.

</dd> <dt>

**bData**
</dt> <dd>

Página del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se anexa a una estructura [**\_ MXDC ESCAPE \_ HEADER \_ T**](mxdcescapeheader.md) (que tiene **su código** de operación establecido en MXDCOP SET S0PAGE) para crear una estructura ESCAPE T DE PASO A TRAVÉS de \_ \_ [**\_ S0PAGE \_ \_ \_ de MXDC.**](mxdcs0pagepassthroughescape.md) Después, esa estructura se pasa al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con [**MXDC \_ ESCAPE**](mxdc-escape.md) como escape. El resultado es que el MXDC pasa la página a la salida sin procesarla.

La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe estar entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

La aplicación que realiza la llamada es responsable de validar el XML de la página del documento XPS.

El consumo de streaming es más eficaz si llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ SET \_ S0PAGE \_ RESOURCE** como **opCode** para cada recurso de la página antes de llamarlo con **MXDCOP \_ SET \_ S0PAGE**.

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

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

