---
description: La función de escape de impresora MXDC ESCAPE permite a las aplicaciones escribir documentos en un archivo o en una impresora en formato XML Paper Specification (XPS) mediante el Convertidor de documentos \_ XPS de Microsoft (MXDC).
ms.assetid: 79aeb32e-94b1-4806-8ebf-a9d0956f4667
title: MXDC_ESCAPE función (Mxdc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_ESCAPE
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7ace79404808db750a15b2c17b6fedb336dbd1d72b1581888324a4d87bb7cd67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460885"
---
# <a name="mxdc_escape-function"></a>Función ESCAPE de MXDC \_

La función de escape de impresora **\_ MXDC ESCAPE** permite a las aplicaciones escribir documentos en un archivo o en una impresora en formato XML Paper Specification (XPS) mediante el Convertidor de documentos XPS de Microsoft (MXDC).

Para realizar esta operación, llame a la [**función ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con los parámetros siguientes.

## <a name="syntax"></a>Sintaxis


```C++
int MXDC_ESCAPE(
    hdc,
    cbInput,
    lpszInData,
    cbOutput,
    lpszOutData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hdc* 
</dt> <dd>

Identificador del contexto del dispositivo de impresora.

</dd> <dt>

*cbInput* 
</dt> <dd>

Tamaño, en bytes, de los datos a los que apunta el *parámetro lpszInData.*

</dd> <dt>

*lpszInData* 
</dt> <dd>

Puntero a un búfer que contiene los datos de entrada, que siempre se almacenan en una de las estructuras siguientes.

<dl> <dd><a href="mxdcescapeheader.md">**MxdcEscapeHeader**</a></dd> <dd><a href="mxdcprintticketescape.md">**MxdcPrintTicketEscape**</a></dd> <dd><a href="mxdcs0pagepassthroughescape.md">**MxdcS0PagePassthroughEscape**</a></dd> <dd><a href="mxdcs0pageresourceescape.md">**MxdcS0PageResourceEscape**</a></dd> </dl>

Cada una de estas estructuras tiene un miembro de código de operación que especifica lo que se supone que debe hacer el MXDC. Consulte MxdcEscapeHeader para obtener comentarios detallados sobre estos códigos.



| Código de operaciones (código de operación)                                                                                                                                                                                                  | Acción                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MXDCOP_GET_FILENAME"></span><span id="mxdcop_get_filename"></span><dl> <dt>**MXDCOP \_ GET \_ FILENAME**</dt> </dl>                                          | Establece el *parámetro lpszOutData* de la función [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) en, ya sea la ruta de acceso completa del archivo de salida como una cadena terminada en cero o el tamaño de esa cadena.<br/>                               |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC_SEQ"></span><span id="mxdcop_printticket_fixed_doc_seq"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC \_ SEQ**</dt> </dl> | Asocia un vale de impresión a una secuencia de documento fijo XPS.<br/>                                                                                                                                                         |
| <span id="MXDCOP_PRINTTICKET_FIXED_DOC"></span><span id="mxdcop_printticket_fixed_doc"></span><dl> <dt>**MXDCOP \_ PRINTTICKET \_ FIXED \_ DOC**</dt> </dl>              | Asocia un vale de impresión a un documento XPS.<br/>                                                                                                                                                                        |
| <span id="MXDCOP_PRINTTICKET_FIXED_PAGE"></span><span id="mxdcop_printticket_fixed_page"></span><dl> <dt>**PÁGINA FIJA \_ DE MXDCOP PRINTTICKET \_ \_**</dt> </dl>           | Asocia un vale de impresión a una página XPS.<br/>                                                                                                                                                                            |
| <span id="MXDCOP_SET_S0PAGE"></span><span id="mxdcop_set_s0page"></span><dl> <dt>**MXDCOP \_ SET \_ S0PAGE**</dt> </dl>                                                | Envía el marcado XPS de la página actual a la salida.<br/>                                                                                                                                                                |
| <span id="MXDCOP_SET_S0PAGE_RESOURCE"></span><span id="mxdcop_set_s0page_resource"></span><dl> <dt>**RECURSO MXDCOP \_ SET \_ \_ S0PAGE**</dt> </dl>                    | Envía un recurso de la página, como una imagen o fuente, a la salida.<br/>                                                                                                                                                 |
| <span id="MXDCOP_SET_XPSPASSTHRU_MODE"></span><span id="mxdcop_set_xpspassthru_mode"></span><dl> <dt>**MXDCOP \_ SET \_ XPSPASSTHRU \_ MODE**</dt> </dl>                 | Coloca el MXDC en un estado de paso a través, lo que permite a una aplicación escribir XPS directamente en el archivo de salida sin ningún procesamiento por parte del MXDC. Se puede escribir de esta manera un documento completo o incluso una secuencia de documentos.<br/> |



 

</dd> <dt>

*cbOutput* 
</dt> <dd>

Tamaño, en bytes, de los datos a los que apunta el *parámetro lpszOutData.*

</dd> <dt>

*lpszOutData* 
</dt> <dd>

Puntero a un búfer que contiene los datos de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es mayor que cero. Si se produce un error en la función o no se admite, el valor devuelto es menor o igual que cero.

## <a name="remarks"></a>Observaciones

Este escape es compatible con MXDC y XPSDrv, pero no con GDI.

Para determinar si el controlador de impresora es el MXDC, llame a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con el escape [**GETTECHNOLOGY.**](/previous-versions/windows/desktop/legacy/dd144931(v=vs.85)) Si el controlador es el MXDC, **ExtEscape** devolverá la cadena terminada en cero, " http://schemas.microsoft.com/xps/2005/06 ". Asegúrese de que el búfer al que hace referencia *el parámetro lpszOutData* es lo suficientemente grande como para contener esta cadena.

Para determinar si el controlador de impresora es el controlador Escritor de documentos XPS de Microsoft Windows en cuadro, confirme que el controlador de impresora es el MXDC y, a continuación, determine si el nombre del controlador de impresora es "Escritor de documentos XPS de Microsoft".

Para obtener el nombre del controlador de impresora, use una de las técnicas siguientes. <dl> Llame [**a GetPrinterDriver con**](getprinterdriver.md) el valor del parámetro *Level* establecido en 1. El nombre del controlador de impresora se devuelve en el **miembro pName** de la [**estructura DRIVER INFO \_ \_ 1.**](driver-info-1.md)  
o  
Llame [**a GetPrinter con**](getprinter.md) el valor del parámetro *Level* establecido en 2. El nombre del controlador de impresora se devuelve en el **miembro pDriverName** de la [**estructura PRINTER INFO \_ \_ 2.**](printer-info-2.md)  
</dl>

En la tabla siguiente se muestra dónde se escribirán varios objetos en el archivo XPS.



| Object       | Ubicación en el archivo de salida    |
|--------------|--------------------------------|
| Página fija   | /Documents/1/Pages/Esc%d.fpage |
| Miniatura    | /Documents/1/Metadata          |
| Imprimir vale | /Documents/1/Metadata          |
| Fuente         | /Documents/1/Resources/Fonts   |
| Imagen        | /Documents/1/Resources/Images  |



 

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

[Funciones de escape de impresora](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))
</dt> <dt>

[**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> </dl>

 

