---
description: La estructura MXDC ESCAPE HEADER T contiene el código de operación para una llamada a ExtEscape con MXDC ESCAPE como \_ \_ parámetro \_ \_ nEscape. También proporciona los tamaños de los búferes de entrada y salida.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T estructura (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE_HEADER_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 53dd83e362ab21938121a986ee2402076d72f870460bc9db608b9a048cee0f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099079"
---
# <a name="mxdc_escape_header_t-structure"></a>Estructura T \_ de ENCABEZADO DE ESCAPE DE \_ \_ MXDC

La **estructura MXDC \_ ESCAPE HEADER \_ \_ T** contiene el código de operación para una llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ ESCAPE**](mxdc-escape.md) como parámetro *nEscape.* También proporciona los tamaños de los búferes de entrada y salida.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMxdcEscapeHeader {
  ULONG cbInput;
  ULONG cbOutput;
  ULONG opCode;
} MXDC_ESCAPE_HEADER_T, *P_MXDC_ESCAPE_HEADER_T;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbInput**
</dt> <dd>

Tamaño del búfer de entrada que se pasará al parámetro *lpszOutData* de la [**función ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)

</dd> <dt>

**cbOutput**
</dt> <dd>

Tamaño del búfer de salida. Este es el mismo valor que el *parámetro cbOutput* de la [**función ExtEscape.**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)

</dd> <dt>

**Opcode**
</dt> <dd>

Constante de código que indica a MXDC qué hacer.



| Código de operaciones                      | Descripción                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ GET \_ FILENAME                | Devuelve, en el parámetro *lpszOutData* de la función [**ExtEscape,**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) la ruta de acceso completa del archivo de salida como una cadena terminada en cero o el tamaño de esa cadena. Vea la sección Comentarios.                   |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ | Asocia un vale de impresión a una secuencia de documento fijo XPS.                                                                                                                                                         |
| MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC      | Asocia un vale de impresión a un documento XPS.                                                                                                                                                                        |
| PÁGINA FIJA \_ DE MXDCOP PRINTTICKET \_ \_     | Asocia un vale de impresión a una página XPS.                                                                                                                                                                            |
| MXDCOP \_ SET \_ S0PAGE                  | Envía el marcado XPS de la página actual a la salida.                                                                                                                                                                |
| RECURSO MXDCOP \_ SET \_ \_ S0PAGE        | Envía un recurso de la página, como una imagen o fuente, a la salida.                                                                                                                                                 |
| MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE       | Coloca el MXDC en un estado de paso a través, lo que permite a una aplicación escribir XPS directamente en el archivo de salida sin ningún procesamiento por parte del MXDC. Se puede escribir de esta manera un documento completo o incluso una secuencia de documentos. |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Antes de [**llamar a MXDC \_ ESCAPE,**](mxdc-escape.md)las aplicaciones deben comprobar primero que el controlador es MXDC mediante una llamada a \_ [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el escape [**GETTECHNOLOGY.**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) Si el controlador es el MXDC, la función devuelve la cadena terminada en cero " http://schemas.microsoft.com/xps/2005/06 ".

Esta estructura siempre está al principio de los datos pasados a la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) en su *parámetro lpszInData.*

Cuando **opCode es** MXDCOP \_ GET \_ FILENAME:

-   El *parámetro lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta solo de la estructura **\_ MXDC ESCAPE HEADER \_ \_ T.**
-   Obtenga el nombre de archivo de salida llamando a [**ExtEscape dos**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) veces.
    1.  La primera vez, pase 4 al *parámetro cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Establezca el *parámetro lpszOutData* para que apunte a los 4 bytes de memoria asignados. El tamaño de la ruta de acceso completa del archivo se devolverá en el parámetro *lpszOutData* de **ExtEscape**.
    2.  A continuación, vuelva a llamar a la función. Esta vez establezca *cbOutput* y *cbInput* en 4+ *DataSize*. La ruta de acceso completa del archivo se devolverá en una [**estructura MxdcGetFileNameData.**](mxdcgetfilenamedata.md)

Cuando **opCode** es MXDCOP \_ PRINTTICKET \_ FIXED DOC \_ \_ SEQ o MXDCOP \_ PRINTTICKET FIXED \_ \_ DOC:

-   El *parámetro lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta de la estructura **MXDC ESCAPE HEADER \_ \_ \_ T** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape.**](mxdcprintticketescape.md)
-   La llamada a [**ExtEscape debe**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Cuando **opCode es** MXDCOP \_ PRINTTICKET FIXED \_ \_ PAGE:

-   El *parámetro lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta de la estructura **MXDC ESCAPE HEADER \_ \_ \_ T** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape.**](mxdcprintticketescape.md)
-   La llamada a [**ExtEscape debe**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Cuando **opCode** es MXDCOP \_ SET \_ S0PAGE:

-   El *parámetro lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta de la estructura **MXDC ESCAPE HEADER \_ \_ \_ T** y una estructura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenada en una estructura [**MxdcS0PagePassthroughEscape.**](mxdcs0pagepassthroughescape.md)
-   La llamada a [**ExtEscape debe**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   La aplicación que realiza la llamada es responsable de validar el XML.
-   El consumo de streaming es más eficaz si llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP SET S0PAGE RESOURCE como opCode para cada recurso de la página antes de llamarlo con \_ \_ \_ MXDCOP  \_ SET \_ S0PAGE.

Cuando **opCode** es MXDCOP \_ SET \_ S0PAGE \_ RESOURCE:

-   El *parámetro lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta de la estructura **MXDC ESCAPE HEADER \_ \_ \_ T** y una estructura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenada en una estructura [**MxdcS0PageResourceEscape.**](mxdcs0pageresourceescape.md)
-   La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), pero puede haber varias llamadas de este tipo entre las llamadas **StartPage** y **EndPage.**
-   El consumo de streaming es más eficaz si llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP SET S0PAGE RESOURCE como opCode para cada recurso de la página antes de llamarlo con \_ \_ \_ MXDCOP  \_ SET \_ S0PAGE.

Cuando **opCode** es MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE:

-   El *parámetro lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) consta solo de la estructura **\_ MXDC ESCAPE HEADER \_ \_ T.**
-   Esta llamada debe producirse antes de la llamada [**a StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

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

 

