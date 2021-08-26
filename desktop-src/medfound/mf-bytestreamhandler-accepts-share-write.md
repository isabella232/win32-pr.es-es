---
description: Especifica si un controlador de flujo de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941035"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ ACEPTA EL atributo SHARE \_ \_ WRITE

Especifica si un controlador de flujo de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Los controladores de flujo de bytes pueden admitir este atributo. Para obtener o establecer el atributo, consulte primero el controlador de flujo de bytes para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) A [**continuación, llame a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**AATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Si este atributo es **TRUE,** significa que el controlador de flujo de bytes puede leer desde una secuencia mientras otro subproceso escribe en la misma secuencia. Cuando otro subproceso abre una secuencia para escribirla, el método [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) devuelve la marca **MFBYTESTREAM \_ SHARE \_ WRITE.**

Este atributo afecta a la resolución de origen. Si una secuencia de bytes tiene establecida la [](source-resolver.md) marca **MFBYTESTREAM \_ SHARE \_ WRITE,** el solucionador de origen no pasará esa secuencia a un controlador de flujo de bytes a menos que el controlador tenga el atributo MF \_ BYTESTREAMHANDLER ACCEPTS SHARE WRITE establecido en \_ \_ \_ **TRUE.**

La **marca MFBYTESTREAM \_ SHARE \_ WRITE** es una sugerencia de que la longitud de la secuencia puede cambiar mientras el controlador lee de ella.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Controladores de esquema y Byte-Stream de esquema](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




