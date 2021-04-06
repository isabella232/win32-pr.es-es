---
description: La \_ estructura MXDC PRINTTICKET \_ Data T contiene \_ un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión y la impresora, para pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: MXDC_PRINTTICKET_DATA_T estructura (Mxdc. h)
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
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909578"
---
# <a name="mxdc_printticket_data_t-structure"></a>Estructura MXDC de \_ datos de PRINTTICKET \_ \_

La estructura **MXDC \_ PRINTTICKET \_ Data \_ T** contiene un vale de impresión de documentos XPS, que contiene la configuración del trabajo de impresión y la impresora, para pasar al archivo de salida del convertidor de documentos XPS de Microsoft (MXDC) sin ningún procesamiento.

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

Tamaño de la solicitud de impresión en bytes.

</dd> <dt>

**bData**
</dt> <dd>

El vale de impresión del documento XPS.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se anexa a una estructura [**de \_ \_ encabezado de \_ escape MXDC**](mxdcescapeheader.md) que tiene el miembro **opCode** establecido en **MXDCOP \_ PrintTicket \_ fixed \_ Page**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** para crear una estructura [**MXDC \_ PrintTicket de \_ escape \_ T**](mxdcprintticketescape.md) . A continuación, se pasa la estructura **MXDC \_ PRINTTICKET de \_ escape \_ T** al parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) cuando se llama con el escape de [**\_ escape MXDC**](mxdc-escape.md) . El efecto es escribir la solicitud de impresión en el archivo de documento XPS.

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

 

