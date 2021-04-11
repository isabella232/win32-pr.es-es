---
description: La \_ estructura del \_ encabezado de escape MXDC \_ contiene el código de operación para una llamada a ExtEscape con MXDC \_ escape como el parámetro nEscape. También proporciona los tamaños de los búferes de entrada y salida.
ms.assetid: 3d1f909c-0c3c-49ac-b530-4ce077ad6d94
title: MXDC_ESCAPE_HEADER_T estructura (Mxdc. h)
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
ms.openlocfilehash: a16e0d5bb1a8ce48e071fe1b32543610d8433e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913146"
---
# <a name="mxdc_escape_header_t-structure"></a>MXDC \_ estructura de escape de \_ encabezado \_ T

La estructura del **\_ \_ encabezado \_ de escape MXDC** contiene el código de operación para una llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con [**MXDC \_ escape**](mxdc-escape.md) como el parámetro *nEscape* . También proporciona los tamaños de los búferes de entrada y salida.

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

Tamaño del búfer de entrada que se pasará al parámetro *lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**cbOutput**
</dt> <dd>

Tamaño del búfer de salida. Este es el mismo valor que el parámetro *cbOutput* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) .

</dd> <dt>

**Código**
</dt> <dd>

Constante de código que indica a MXDC qué hacer.



| Código de operaciones                      | Descripción                                                                                                                                                                                                            |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MXDCOP \_ Get \_ nombreDeArchivo                | Devuelve, en el parámetro *lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) , la ruta de acceso completa del archivo de salida como una cadena terminada en cero o el tamaño de esa cadena. Vea la sección Comentarios.                   |
| MXDCOP \_ de \_ documento fijo de PRINTTICKET fijo \_ \_ | Asocia una incidencia de impresión a una secuencia de documento fijo XPS.                                                                                                                                                         |
| \_ \_ documento fijo de PRINTTICKET MXDCOP \_      | Asocia una incidencia de impresión a un documento XPS.                                                                                                                                                                        |
| MXDCOP \_ \_ Página fija de PRINTTICKET \_     | Asocia una incidencia de impresión a una página XPS.                                                                                                                                                                            |
| MXDCOP \_ establecer \_ S0PAGE                  | Envía el marcado XPS de la página actual a la salida.                                                                                                                                                                |
| \_Recurso MXDCOP set \_ S0PAGE \_        | Envía a la salida un recurso de la página, como una imagen o fuente.                                                                                                                                                 |
| MXDCOP \_ set \_ XPSPASSTHRU \_ Mode       | Coloca el MXDC en un estado de paso a través, lo que permite que una aplicación escriba XPS directamente en el archivo de salida sin ningún procesamiento por parte de MXDC. Se puede escribir un documento completo o incluso una secuencia de documento de esta manera. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Antes de llamar a [**MXDC \_ escape**](mxdc-escape.md), \_ las aplicaciones deben comprobar primero que el controlador se MXDC llamando a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el escape [**GETTECHNOLOGY**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) . Si el controlador es MXDC, la función devuelve la cadena terminada en cero " http://schemas.microsoft.com/xps/2005/06 ".

Esta estructura siempre está al principio de los datos pasados a la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) en su parámetro *lpszInData* .

Cuando **opCode** es MXDCOP \_ Get \_ filename:

-   El parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) solo se compone de la estructura **\_ \_ \_ T del encabezado de escape MXDC** .
-   Para obtener el nombre de archivo de salida, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) dos veces.
    1.  La primera vez, pase 4 al parámetro *cbOutput* de [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape). Establezca el parámetro *lpszOutData* para que apunte a cualquier 4 bytes de memoria asignados. El tamaño de la ruta de acceso completa del archivo se devolverá en el parámetro *lpszOutData* de **ExtEscape**.
    2.  A continuación, llame de nuevo a la función. Esta vez, establezca *cbOutput* y *cbInput* en 4 + *datasize*. La ruta de acceso completa del archivo se devolverá en una estructura [**MxdcGetFileNameData**](mxdcgetfilenamedata.md) .

Cuando **opCode** es MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq o MXDCOP \_ PrintTicket \_ fixed \_ doc:

-   El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) y una llamada a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).

Cuando **opCode** es MXDCOP \_ \_ Página fija de PRINTTICKET \_ :

-   El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcPrintTicketPassthrough**](mxdcprintticketpassthrough.md) concatenada en una estructura [**MxdcPrintTicketEscape**](mxdcprintticketescape.md) .
-   La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).

Cuando **opCode** es MXDCOP \_ set \_ S0PAGE:

-   El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcS0PageData**](mxdcs0pagedata.md) concatenada en una estructura [**MxdcS0PagePassthroughEscape**](mxdcs0pagepassthroughescape.md) .
-   La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).
-   La aplicación que realiza la llamada es responsable de validar el XML.
-   El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ set \_ S0PAGE \_ Resource como **opCode** para cada recurso de la página antes de llamarlo con MXDCOP \_ set \_ S0PAGE.

Cuando **opCode** es MXDCOP \_ set \_ S0PAGE \_ Resource:

-   El parámetro *lpszInData* de la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) está compuesto de la estructura MXDC de **\_ encabezado de escape \_ \_** y una estructura [**MxdcXpsS0PageResource**](mxdcxpss0pageresource.md) concatenada en una estructura [**MxdcS0PageResourceEscape**](mxdcs0pageresourceescape.md) .
-   La llamada a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) debe producirse entre una llamada a [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) y una llamada a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage), pero puede haber varias llamadas de este tipo entre las llamadas a **StartPage** y **EndPage** .
-   El consumo de streaming es más eficaz si se llama a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con MXDCOP \_ set \_ S0PAGE \_ Resource como **opCode** para cada recurso de la página antes de llamarlo con MXDCOP \_ set \_ S0PAGE.

Cuando **opCode** es MXDCOP \_ set \_ XPSPASSTHRU \_ Mode:

-   El parámetro *lpszInData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) solo se compone de la estructura **\_ \_ \_ T del encabezado de escape MXDC** .
-   Esta llamada debe realizarse antes de la llamada a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca).

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

 

