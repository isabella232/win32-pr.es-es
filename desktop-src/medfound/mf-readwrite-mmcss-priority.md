---
description: Establece la prioridad del subproceso base para el lector de origen o el escritor de receptores.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: MF_READWRITE_MMCSS_PRIORITY atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740607"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>Atributo \_ MF READWRITE \_ MMCSS \_ PRIORITY

Establece la prioridad del subproceso base para el lector de origen o el escritor de receptores.

## <a name="data-type"></a>Tipo de datos

**INT32 almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Opcionalmente, establezca este atributo al crear una instancia del lector de [origen](source-reader.md) o del [escritor de receptores.](sink-writer.md) Si establece este atributo, establezca también el atributo [MF \_ READWRITE \_ MMCSS \_ CLASS.](mf-readwrite-mmcss-class.md) De lo contrario, se omite este atributo.

Cuando el lector de origen o el escritor de receptores registran subprocesos con el servicio Programador de clases [multimedia](../procthread/multimedia-class-scheduler-service.md), el valor de este atributo especifica la prioridad del subproceso base. Si no se establece este atributo, el valor predeterminado es cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
