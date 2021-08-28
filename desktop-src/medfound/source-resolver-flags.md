---
description: Define el comportamiento del solucionador de origen. Estos marcadores también los usan los controladores de esquema y los controladores de secuencias de bytes.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Marcas de resolución de origen (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847825"
---
# <a name="source-resolver-flags"></a>Marcas de resolución de origen

Define el comportamiento del solucionador de origen. Estos marcadores también los usan los controladores de esquema y los controladores de secuencias de bytes.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ Solución \_ de problemas de MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Intente crear un origen multimedia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ Resolución \_ de la secuencia de**</dt> bytes <dt>0x00000002</dt> </dl>                                                                                                                                              | Intente crear una secuencia de bytes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **EL \_ CONTENIDO DE LA RESOLUCIÓN MF NO TIENE QUE \_ COINCIDIR CON LA EXTENSIÓN O \_ EL \_ \_ \_ \_ \_ \_ \_ \_ TIPO MIME**</dt> <dt>0x00000010</dt> </dl> | Si se produce un error en la resolución de origen mediante el controlador de secuencia de bytes registrado para el tipo MIME o la extensión de nombre de archivo, el solucionador de origen enumera todos los controladores de flujo de bytes registrados.<br/> Los controladores de flujo de bytes se registran mediante la extensión de nombre de archivo o el tipo MIME. Inicialmente, la resolución de origen intenta usar un controlador que coincida con la extensión de nombre de archivo o el tipo MIME. Si se produce un error, se produce un error en toda la resolución de origen de forma predeterminada y la resolución de origen devuelve un código de error a la aplicación. Sin embargo, si se especifica esta marca, el solucionador de origen continúa enumerando a través de todos los controladores de flujo de bytes registrados. Posiblemente, un controlador con coincidencias erróneas puede crear correctamente el origen multimedia.<br/> Esta marca no se puede combinar con la marca MF \_ RESOLUTION KEEP BYTE STREAM ALIVE ON \_ \_ \_ \_ \_ \_ FAIL. Vea Comentarios para obtener más información.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ RESOLUCIÓN \_ MANTENGA LA SECUENCIA DE BYTES ACTIVO EN CASO \_ \_ \_ \_ \_ DE**</dt> <dt>ERROR 0x00000020</dt> </dl>                                                                             | Si se produce un error en la resolución de origen, la resolución de origen no cierra la secuencia de bytes. De forma predeterminada, el solucionador de origen cierra la secuencia de bytes en caso de error.<br/> Si se usa esta marca y se produce un error en la resolución de origen, el autor de la llamada debe llamar de nuevo al método y establecer la marca MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION \_ OR MIME \_ TYPE \_ \_ \_ \_ \_ \_ \_ \_ .<br/> Esta marca no se puede combinar con la marca MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION O \_ MIME \_ \_ \_ \_ \_ \_ \_ \_ \_ TYPE. Vea Comentarios para obtener más información.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ Resolución \_ de lectura**</dt> <dt>0x00010000</dt> </dl>                                                                                                                                                                | Solicita acceso de lectura al origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ Resolución \_ de escritura**</dt> <dt>0x00020000</dt> </dl>                                                                                                                                                             | Solicita acceso de escritura al origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ RESOLUCIÓN \_ DESHABILITAR \_ COMPLEMENTOS \_ LOCALES**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | El solucionador de origen no usará el esquema registrado localmente ni los complementos del controlador de secuencia de bytes.<br/> Requiere Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Comentarios

La aplicación establece estas marcas cuando usa la interfaz [**DEFUSSOURCEResolver.**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) El solucionador de origen pasa las mismas marcas a los métodos [**IMFByteStreamHandler::BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) y [**IMFSchemeHandler::BeginCreateObject.**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)

Debe especificar una de las marcas MF \_ RESOLUTION \_ MEDIASOURCE o MF \_ RESOLUTION \_ BYTESTREAM. Todas las marcas restantes son opcionales.

La marca KEEP BYTE STREAM ALIVE ON FAIL de MF \_ RESOLUTION se define para el escenario \_ \_ \_ \_ \_ \_ siguiente:

1.  La aplicación intenta abrir un origen a través de la red. La aplicación establece la marca KEEP BYTE STREAM ALIVE ON FAIL de MF \_ \_ \_ \_ \_ \_ \_ RESOLUTION.

2.  La dirección URL del origen contiene la extensión de nombre de archivo incorrecta. Dado que la extensión de nombre de archivo es incorrecta, el controlador predeterminado de secuencia de bytes no puede crear el origen multimedia. Dado que la aplicación establece la marca MF \_ RESOLUTION KEEP BYTE STREAM ALIVE ON \_ FAIL, la resolución de origen almacena en caché \_ la secuencia de \_ \_ \_ \_ bytes.

3.  La resolución de origen devuelve un código de error a la aplicación.

4.  El cliente vuelve a abrir el origen, esta vez estableciendo la marca MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION O \_ MIME \_ \_ \_ \_ \_ \_ \_ \_ \_ TYPE. Esta marca hace que el solucionador de origen pruebe todos los controladores registrados en lugar de solo el controlador predeterminado. Dado que la secuencia de bytes se ha almacenado en caché, la resolución de origen no tiene que volver a abrir la secuencia de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 




