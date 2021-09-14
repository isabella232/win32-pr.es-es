---
title: Valores devueltos del almacén de texto (Textstor.h)
description: Cuando un administrador de documentos procesa un almacén de texto, genera valores devueltos en el intervalo de 0xHHHH0200 a 0xHHHH0300. En la tabla siguiente se enumeran los valores devueltos del almacén de texto en orden alfabético.
ms.assetid: 20b0a89f-ab52-466f-9669-c6c29ad12de0
topic_type:
- apiref
api_name:
- Text Store Return Values
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc2e0141eea559371411455973f1fa4aa87f31e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068808"
---
# <a name="text-store-return-values"></a>Valores devueltos del almacén de texto

Cuando un administrador de documentos procesa un almacén de texto, genera valores devueltos en el intervalo de 0x *HHHH* 0200 a 0x *HHHH* 0300. En la tabla siguiente se enumeran los valores devueltos del almacén de texto en orden alfabético.



| Código o valor devuelto                                                                                                                                                                                                                          | Descripción                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_E_FORMAT"></span><span id="ts_e_format"></span><dl> <dt>**TS \_ E \_ FORMAT**</dt> <dt>0x8004020a</dt> </dl>                   | La aplicación no admite el tipo de datos contenido en el [**objeto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) que se va a insertar [**mediante ITextStoreACP::InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded).<br/> |
| <span id="TS_E_INVALIDPOINT"></span><span id="ts_e_invalidpoint"></span><dl> <dt>**TS \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl> | El parámetro no está dentro del cuadro de límite de ningún carácter.<br/>                                                                                                                                        |
| <span id="TS_E_INVALIDPOS"></span><span id="ts_e_invalidpos"></span><dl> <dt>**TS \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>       | El intervalo especificado se extiende fuera del documento.<br/>                                                                                                                                                     |
| <span id="TS_E_NOINTERFACE"></span><span id="ts_e_nointerface"></span><dl> <dt>**TS \_ E \_ NOINTERFACE**</dt> <dt>0x80040204</dt> </dl>    | El objeto no admite la interfaz solicitada.<br/>                                                                                                                                                  |
| <span id="TS_E_NOLAYOUT"></span><span id="ts_e_nolayout"></span><dl> <dt>**TS \_ E \_ NOLAYOUT**</dt> <dt>0x80040206</dt> </dl>             | La aplicación no ha calculado un diseño de texto.<br/>                                                                                                                                                     |
| <span id="TS_E_NOLOCK"></span><span id="ts_e_nolock"></span><dl> <dt>**TS \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                   | La aplicación no tiene un bloqueo de solo lectura ni un bloqueo de lectura y escritura para el documento.<br/>                                                                                                                   |
| <span id="TS_E_NOOBJECT"></span><span id="ts_e_noobject"></span><dl> <dt>**TS \_ E \_ NOOBJECT**</dt> <dt>0x80040202</dt> </dl>             | El desplazamiento de contenido insertado no se coloca delante de un \_ carácter TF CHAR \_ EMBEDDED.<br/>                                                                                                                  |
| <span id="TS_E_NOSELECTION"></span><span id="ts_e_noselection"></span><dl> <dt>**TS \_ E \_ NOSELECTION**</dt> <dt>0x80040205</dt> </dl>    | El documento no tiene selección.<br/>                                                                                                                                                                        |
| <span id="TS_E_NOSERVICE"></span><span id="ts_e_noservice"></span><dl> <dt>**TS \_ E \_ NOSERVICE**</dt> <dt>0x80040203</dt> </dl>          | No se puede devolver contenido para que coincida con el GUID del servicio.<br/>                                                                                                                                             |
| <span id="TS_E_READONLY"></span><span id="ts_e_readonly"></span><dl> <dt>**TS \_ E \_ READONLY**</dt> <dt>0x80040209</dt> </dl>             | El documento es de solo lectura. No se puede modificar el contenido.<br/>                                                                                                                                                     |
| <span id="TS_E_SYNCHRONOUS"></span><span id="ts_e_synchronous"></span><dl> <dt>**TS \_ E \_ SYNCHRONOUS**</dt> <dt>0x00040300</dt> </dl>    | El documento no se puede bloquear sincrónicamente.<br/>                                                                                                                                                          |
| <span id="TS_S_ASYNC"></span><span id="ts_s_async"></span><dl> <dt>**TS \_ S \_ ASYNC**</dt> <dt>( 0x1 )</dt> </dl>                         | El documento recibió correctamente un bloqueo asincrónico.<br/>                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITextStoreACP::InsertEmbedded**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> </dl>

 

