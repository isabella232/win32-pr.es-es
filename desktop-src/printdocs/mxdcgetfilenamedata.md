---
description: La estructura GET FILENAME DATA T de MXDC contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del Convertidor de documentos \_ \_ \_ \_ XPS de Microsoft (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: MXDC_GET_FILENAME_DATA_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ef0b29590b4a9080e943fae5c3e78fb18a99232a2a531a80b63b303b28c2bea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948345"
---
# <a name="mxdc_get_filename_data_t-structure"></a>ESTRUCTURA DE T DE DATOS DE MXDC \_ GET \_ FILENAME \_ \_

La **estructura GET FILENAME DATA \_ \_ \_ \_ T** de MXDC contiene la ruta de acceso completa y el nombre de archivo de un archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbOutput**
</dt> <dd>

Tamaño del búfer de salida, **wszData.**

</dd> <dt>

**wszData**
</dt> <dd>

Ruta de acceso completa y nombre de archivo del archivo de salida.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) devuelve esta estructura cuando se llama con el escape ESCAPE de [**\_ MXDC**](mxdc-escape.md) y la estructura [**MXDC ESCAPE HEADER \_ \_ \_ T**](mxdcescapeheader.md) que se pasa en el parámetro *lpszInData* tiene su **opCode** establecido en **MXDCOP \_ GET \_ FILENAME**.

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

 

