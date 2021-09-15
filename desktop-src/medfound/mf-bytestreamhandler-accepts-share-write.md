---
description: Especifica si un controlador de flujo de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474227"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ ACEPTA EL atributo SHARE \_ \_ WRITE

Especifica si un controlador de flujo de bytes puede usar una secuencia de bytes abierta para que la escriba otro subproceso.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Los controladores de flujo de bytes pueden admitir este atributo. Para obtener o establecer el atributo, consulte primero el controlador de flujo de bytes para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) A [**continuación, llame a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) [**o AATTRIBUTEAttributes::SetUINT32.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Si este atributo es **TRUE,** significa que el controlador de flujo de bytes puede leer desde una secuencia mientras otro subproceso escribe en la misma secuencia. Cuando otro subproceso abre una secuencia para escribirla, el método [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) devuelve la marca **MFBYTESTREAM \_ SHARE \_ WRITE.**

Este atributo afecta a la resolución de origen. Si una secuencia de bytes tiene establecida la [](source-resolver.md) marca **MFBYTESTREAM \_ SHARE \_ WRITE,** el solucionador de origen no pasará esa secuencia a un controlador de flujo de bytes a menos que el controlador tenga el atributo MF \_ BYTESTREAMHANDLER ACCEPTS SHARE WRITE establecido en \_ \_ \_ **TRUE.**

La **marca MFBYTESTREAM \_ SHARE \_ WRITE** es una sugerencia de que la longitud de la secuencia puede cambiar mientras el controlador lee de ella.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Controladores de esquemas y Byte-Stream de esquema](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




