---
description: Especifica si el escritor del receptor limita la velocidad de los datos entrantes.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: MF_SINK_WRITER_DISABLE_THROTTLING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716952"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a>\_Atributo de \_ \_ limitación de deshabilitación del escritor de receptor MF \_

Especifica si el escritor del receptor limita la velocidad de los datos entrantes.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

De forma predeterminada, el método [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) del escritor receptor limita la velocidad de los datos bloqueando el subproceso que realiza la llamada. Esto evita que la aplicación entregue los ejemplos demasiado rápido. Para deshabilitar este comportamiento, establezca el \_ atributo de limitación del escritor del receptor MF \_ \_ \_ en **true** cuando cree el escritor del receptor.

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del escritor de receptor](sink-writer-attributes.md)
</dt> </dl>

 

 




