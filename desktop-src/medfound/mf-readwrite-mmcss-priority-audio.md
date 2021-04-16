---
description: Establece la prioridad base para los subprocesos de procesamiento de audio creados por el lector de origen o el escritor del receptor.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: MF_READWRITE_MMCSS_PRIORITY_AUDIO atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705798"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>MF \_ ReadWrite \_ / \_ atributo de audio prioritario de MMCSS \_

Establece la prioridad base para los subprocesos de procesamiento de audio creados por el lector de origen o el escritor del receptor.

## <a name="data-type"></a>Tipo de datos

**INT32** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md). Si establece este atributo, establezca también el atributo de audio de la [ \_ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) . De lo contrario, se omite este atributo.

Cuando el lector de origen o el escritor receptor registra los subprocesos de procesamiento de audio con el [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md), el valor de este atributo especifica la prioridad de subproceso base. Si no se establece este atributo, el valor predeterminado es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
