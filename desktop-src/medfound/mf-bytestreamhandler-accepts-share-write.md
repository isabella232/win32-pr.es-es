---
description: Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso pueda escribir en él.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687216"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ acepta el \_ atributo de escritura de recurso compartido \_

Especifica si un controlador de flujo de bytes puede utilizar un flujo de bytes abierto para que otro subproceso pueda escribir en él.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Los controladores de secuencias de bytes pueden admitir este atributo. Para obtener o establecer el atributo, primero consulte el controlador de flujo de bytes para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Después, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Si este atributo es **true**, significa que el controlador de flujo de bytes puede leer de una secuencia mientras otro subproceso escribe en la misma secuencia. Cuando un flujo se abre para escribir en otro subproceso, el método [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) devuelve la marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** .

Este atributo afecta a la resolución de código fuente. Si una secuencia de bytes tiene establecida la marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** , la [resolución de origen](source-resolver.md) no pasará esa secuencia a un controlador de flujo de bytes a menos que el controlador tenga el \_ atributo MF BYTESTREAMHANDLER acepte el atributo de \_ \_ recurso compartido de \_ escritura establecido en **true**.

La marca de **\_ \_ escritura de recurso compartido MFBYTESTREAM** es una sugerencia de que la longitud de la secuencia podría cambiar mientras el controlador Lee de ella.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                     |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Controladores de esquema y controladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




