---
description: Especifica una clase del Servicio programador de clases multimedia (MMCSS) para subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467211"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>Atributo \_ AUDIO MF READWRITE \_ MMCSS \_ CLASS \_

Especifica una clase [del Servicio programador de](../procthread/multimedia-class-scheduler-service.md) clases multimedia (MMCSS) para subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del lector de [origen](source-reader.md) o del [escritor de receptores.](sink-writer.md) El valor del atributo debe ser un nombre de clase MMCSS válido.

Si se establece este atributo, el lector de origen o el escritor receptor registran sus subprocesos de procesamiento de audio con la clase MMCSS especificada. MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tiene prioridad sobre otras tareas del sistema.

Para especificar la prioridad base de los subprocesos de audio, establezca el atributo [MF \_ READWRITE \_ MMCSS \_ PRIORITY \_ AUDIO.](mf-readwrite-mmcss-priority-audio.md) Si no se establece ese atributo, la prioridad base para los subprocesos de audio es cero.

Este atributo invalida el atributo [MF \_ READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md) para subprocesos de procesamiento de audio. Si no se establece ningún atributo, los subprocesos de audio no se registran con MCSS.

En la mayoría de las aplicaciones, los problemas de audio son mucho más perceptibles para el usuario que los problemas de vídeo y, por tanto, menos aceptables. Por este motivo, una aplicación normalmente debe establecer MF READWRITE MMCSS CLASS AUDIO en una clase MMCSS de prioridad más alta que \_ \_ MF \_ \_ [ \_ READWRITE \_ MMCSS \_ CLASS](mf-readwrite-mmcss-class.md). Esto garantiza que el procesamiento de audio tiene mayor prioridad que otras tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
