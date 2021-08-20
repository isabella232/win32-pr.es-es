---
description: Especifica una clase del Servicio programador de clases multimedia (MMCSS) para el lector de origen o el escritor de receptores.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d9fccedd9005404c48ddb614db5240d823fe19647b2c1850ae59b41a6dd165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876168"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>Atributo \_ MF READWRITE \_ MMCSS \_ CLASS

Especifica una clase [del Servicio programador de](../procthread/multimedia-class-scheduler-service.md) clases multimedia (MMCSS) para el lector de origen o el escritor de receptores.

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentarios

Opcionalmente, establezca este atributo al crear una instancia del lector de [origen o](source-reader.md) del escritor [de receptores.](sink-writer.md) El valor del atributo debe ser un nombre de clase MMCSS válido.

Si se establece este atributo, el lector de origen o el escritor receptor registran todos sus subprocesos con la clase MMCSS especificada. MMCSS garantiza que el procesamiento de datos en el Lector de origen o el Escritor de receptores tiene prioridad sobre otras tareas del sistema.

Para especificar la prioridad base, establezca el atributo [MF \_ READWRITE \_ MMCSS \_ PRIORITY.](mf-readwrite-mmcss-priority.md) Si no se establece ese atributo, la prioridad base es cero.

Para los subprocesos de procesamiento de audio, el atributo [ \_ MF READWRITE \_ MMCSS \_ CLASS \_ AUDIO](mf-readwrite-mmcss-class-audio.md) (si se establece) invalida este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
