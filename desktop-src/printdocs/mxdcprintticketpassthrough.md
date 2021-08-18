---
description: La estructura MXDC PRINTTICKET DATA T contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión e impresora, para pasar al archivo de salida del Convertidor de documentos \_ \_ \_ XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 3cf778781340323a78495f87b1408e1011641797ed52a3565bafe41ca450d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471657"
---
# <a name="mxdc_printticket_data_t-structure"></a>Estructura DE \_ T DE DATOS DE MXDC \_ \_ PRINTTICKET

La estructura **MXDC \_ PRINTTICKET \_ DATA \_ T** contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión e impresora, para pasar al archivo de salida del Convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwDataSize**
</dt> <dd>

Tamaño del vale de impresión en bytes.

</dd> <dt>

**bData**
</dt> <dd>

El vale de impresión del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se anexa a una estructura [**MXDC \_ ESCAPE HEADER \_ \_ T**](mxdcescapeheader.md) que tiene el miembro **opCode** establecido en **MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE**, **MXDCOP \_ PRINTTICKET FIXED \_ \_ DOC** o **MXDCOP \_ PRINTTICKET FIXED DOC \_ \_ \_ SEQ** para crear una estructura [**\_ MXDC PRINTTICKET \_ ESCAPE \_ T.**](mxdcprintticketescape.md) A continuación, la estructura **MXDC \_ PRINTTICKET \_ ESCAPE \_ T** se pasa al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape [**ESCAPE \_ de MXDC.**](mxdc-escape.md) El efecto es escribir el vale de impresión en el archivo de documento XPS.

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

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[Funciones de escape de impresora GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[**MXDC \_ ESCAPE**](mxdc-escape.md)
</dt> </dl>

 

