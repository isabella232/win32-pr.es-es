---
description: Especifica si un búfer contiene el inicio de un paquete de formato de sistemas avanzados (ASF).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY atributo (Wmcontainer.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363871"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>Atributo PACKET BOUNDARY de MFASFSPLITTER \_ \_

Especifica si un búfer contiene el inicio de un paquete de formato de sistemas avanzados (ASF).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Si un búfer multimedia expone la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a través de **QueryInterface** y el valor de este atributo es distinto de cero, el divisor ASF trata el búfer como el inicio de un nuevo paquete.

Este atributo se aplica si usa el divisor ASF para analizar los datos de ASF. Si los datos de ASF tienen longitudes de paquete variables, debe establecer este atributo en los búferes multimedia que se pasan al método [**IMFASFSplitter::P arseData.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) Establezca el atributo en **TRUE** si el búfer contiene el inicio de un nuevo paquete. Si el búfer contiene una continuación del paquete anterior, establezca el atributo en **FALSE.** Los búferes no pueden abarcar varios paquetes.

Para los datos de ASF con tamaños fijos de paquete, este atributo no es necesario y un búfer puede abarcar varios paquetes.

Tenga en cuenta que las implementaciones estándar de [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) proporcionadas por Media Foundation no exponen [**LOSATTRIBUTE.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Para usar este atributo, debe proporcionar su propia implementación de **IMFMediaBuffer**; por ejemplo, ajustando los búferes devueltos [**por MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de ASF](asf-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




