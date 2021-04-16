---
description: Especifica una clase de servicio de programador de clases multimedia (MMCSS) para los subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: MF_READWRITE_MMCSS_CLASS_AUDIO atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705799"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>MF \_ ReadWrite \_ \_ Class ( \_ atributo de audio)

Especifica una clase de [servicio de programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para los subprocesos de procesamiento de audio en el lector de origen o el escritor de receptores.

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md). El valor del atributo debe ser un nombre de clase MMCSS válido.

Si se establece este atributo, el lector de origen o el escritor receptor registra sus subprocesos de procesamiento de audio con la clase MMCSS especificada. MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tenga prioridad sobre otras tareas del sistema.

Para especificar la prioridad base para los subprocesos de audio, establezca el atributo de [ \_ audio MF ReadWrite en \_ \_ prioridad \_ ](mf-readwrite-mmcss-priority-audio.md) . Si no se establece ese atributo, la prioridad base para los subprocesos de audio es cero.

Este atributo invalida el atributo de [ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) para los subprocesos de procesamiento de audio. Si no se establece ningún atributo, los subprocesos de audio no se registran con MCSS.

Para la mayoría de las aplicaciones, el problema de audio es mucho más perceptible para el usuario que el problema de vídeo y, por lo tanto, menos aceptable. Por esta razón, una aplicación normalmente debe establecer el \_ audio de la clase MF ReadWrite \_ MMCSS \_ \_ en una clase MMCSS de mayor prioridad que la [ \_ clase MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md). Esto garantiza que el procesamiento de audio tenga mayor prioridad que otras tareas.

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

 

 
