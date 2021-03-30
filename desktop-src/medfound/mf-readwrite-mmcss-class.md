---
description: Especifica una clase de servicio del programador de clases multimedia (MMCSS) para el lector de origen o el escritor del receptor.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: MF_READWRITE_MMCSS_CLASS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817126"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>MF \_ ReadWrite \_ ( \_ atributo de clase)

Especifica una clase de [servicio del programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) para el lector de origen o el escritor del receptor.

## <a name="data-type"></a>Tipo de datos

**LPWSTR**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del [lector de origen](source-reader.md) o del [escritor de receptores](sink-writer.md). El valor del atributo debe ser un nombre de clase MMCSS válido.

Si se establece este atributo, el lector de origen o el escritor receptor registra todos los subprocesos con la clase MMCSS especificada. MMCSS garantiza que el procesamiento de datos en el lector de origen o el escritor de receptores tenga prioridad sobre otras tareas del sistema.

Para especificar la prioridad base, establezca el atributo de [ \_ \_ \_ prioridad MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) . Si no se establece ese atributo, la prioridad base es cero.

En el caso de los subprocesos de procesamiento de audio, el atributo de audio de la [ \_ \_ \_ \_ clase MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) (si se establece) invalida este atributo.

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

 

 
