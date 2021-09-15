---
description: Especifica una clase del Servicio programador de clases multimedia (MMCSS) para el lector de origen o el escritor de receptores.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475717"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>Atributo \_ MF READWRITE \_ MMCSS \_ CLASS

Especifica una clase [del Servicio programador de](../procthread/multimedia-class-scheduler-service.md) clases multimedia (MMCSS) para el lector de origen o el escritor de receptores.

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del lector de [origen](source-reader.md) o del [escritor de receptores.](sink-writer.md) El valor del atributo debe ser un nombre de clase MMCSS válido.

Si se establece este atributo, el lector de origen o el escritor de receptores registran todos sus subprocesos con la clase MMCSS especificada. MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tiene prioridad sobre otras tareas del sistema.

Para especificar la prioridad base, establezca el atributo [MF \_ READWRITE \_ MMCSS \_ PRIORITY.](mf-readwrite-mmcss-priority.md) Si no se establece ese atributo, la prioridad base es cero.

En el caso de los subprocesos de procesamiento de audio, el atributo [ \_ MF READWRITE \_ MMCSS \_ CLASS \_ AUDIO](mf-readwrite-mmcss-class-audio.md) (si se establece) invalida este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
