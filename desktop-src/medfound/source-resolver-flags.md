---
description: Define el comportamiento de la resolución de origen. Estos marcadores también los usan los controladores de esquema y los controladores de secuencias de bytes.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Marcas de resolución de origen (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31efe47f75151f78958903cb514653edb6c5aa08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811545"
---
# <a name="source-resolver-flags"></a>Marcas de resolución de origen

Define el comportamiento de la resolución de origen. Estos marcadores también los usan los controladores de esquema y los controladores de secuencias de bytes.



| Constante o valor                                                                                                                                                                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ Resolution \_ MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Intente crear un origen de medios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ RESOLUCIÓN \_ BYTESTREAM**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Intento de crear una secuencia de bytes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> El <dt> **\_ contenido de la resolución MF \_ \_ \_ no \_ tiene \_ que \_ coincidir con la \_ extensión o el \_ \_ \_ tipo MIME**</dt> <dt>0x00000010</dt> </dl> | Si se produce un error en la resolución de origen mediante el controlador de flujo de bytes registrado para el tipo MIME o la extensión de nombre de archivo, la resolución de origen enumera todos los controladores de flujo de bytes registrados.<br/> Los controladores de secuencias de bytes se registran mediante la extensión de nombre de archivo o el tipo MIME. Inicialmente, el solucionador de origen intenta utilizar un controlador que coincide con la extensión de nombre de archivo o el tipo MIME. Si se produce un error, de forma predeterminada se produce un error en la resolución de origen completa y la resolución de origen devuelve un código de error a la aplicación. Sin embargo, si se especifica esta marca, la resolución de origen sigue enumerando todos los controladores de flujo de bytes registrados. Es posible que un controlador sin coincidencia pueda crear correctamente el origen de medios.<br/> Esta marca no se puede combinar con el \_ \_ marcador de \_ \_ retransmisión de la secuencia de bytes \_ \_ de \_ Resolution Vea Comentarios para obtener más información.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ La resolución \_ mantiene el \_ \_ flujo de bytes \_ activo \_ en \_ FAIL**</dt> <dt>0x00000020</dt> </dl>                                                                             | Si se produce un error en la resolución de origen, la resolución de origen no cierra la secuencia de bytes. De forma predeterminada, la resolución de origen cierra el flujo de bytes en caso de error.<br/> Si se usa esta marca y se produce un error en la resolución de origen, el llamador debe volver a llamar al método y establecer que el \_ contenido de resolución MF \_ \_ \_ no \_ tenga \_ que coincidir con la \_ \_ \_ marca o el \_ \_ tipo MIME.<br/> Esta marca no se puede combinar con el \_ contenido de resolución MF \_ \_ \_ no \_ tiene \_ que \_ coincidir con la \_ \_ marca o el \_ \_ tipo MIME. Vea Comentarios para obtener más información.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ RESOLUCIÓN de \_ lectura**</dt> <dt>0x00010000</dt> </dl>                                                                                                                                                                | Solicita acceso de lectura al origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ 0x00020000 de \_ escritura de resolución**</dt> <dt></dt> </dl>                                                                                                                                                             | Solicita acceso de escritura al origen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ RESOLUCIÓN \_ deshabilitar \_ \_ Complementos locales**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | La resolución de origen no usará complementos de controlador de bytestream o esquema registrados localmente.<br/> Requiere Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Observaciones

La aplicación establece estas marcas cuando usa la interfaz [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) . La resolución de origen pasa las mismas marcas a los métodos [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) y [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) .

Debe especificar una de las marcas BYTESTREAM de Resolution \_ \_ MEDIASOURCE o MF \_ Resolution \_ . Todas las marcas restantes son opcionales.

El \_ indicador de \_ retransmisión Resolution \_ de bytes Keep \_ \_ Alive \_ on \_ FAIL se define para el siguiente escenario:

1.  La aplicación intenta abrir un origen a través de la red. La aplicación establece la \_ resolución MF \_ para mantener el \_ \_ flujo de bytes \_ activo en el \_ \_ indicador de error.

2.  La dirección URL del origen contiene una extensión de nombre de archivo incorrecta. Dado que la extensión de nombre de archivo es incorrecta, el controlador de secuencias de bytes predeterminado no puede crear el origen de medios. Dado que la aplicación ha establecido que la \_ resolución MF \_ mantenga el \_ \_ flujo de bytes \_ activo en el \_ \_ indicador de error, la resolución de origen almacena en caché el flujo de bytes.

3.  La resolución de origen devuelve un código de error a la aplicación.

4.  El cliente vuelve a abrir el origen; esta vez, \_ no es necesario que el contenido de la resolución MF \_ \_ \_ \_ \_ \_ coincida con la \_ \_ \_ marca de tipo MIME o extensión \_ . Esta marca hace que la resolución de origen pruebe todos los controladores registrados en lugar de solo el controlador predeterminado. Dado que la secuencia de bytes se almacenó en caché, la resolución de origen no tiene que volver a abrir la secuencia de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Media Foundation](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Solucionador de origen](source-resolver.md)
</dt> </dl>

 

 




