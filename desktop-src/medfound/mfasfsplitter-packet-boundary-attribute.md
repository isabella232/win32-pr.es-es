---
description: Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: MFASFSPLITTER_PACKET_BOUNDARY atributo (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648226"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>Atributo de límite de \_ paquetes de MFASFSPLITTER \_

Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF).

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Si un búfer multimedia expone la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a través de **QueryInterface** y el valor de este atributo es distinto de cero, el divisor de ASF trata el búfer como el inicio de un nuevo paquete.

Este atributo se aplica si usa el divisor de ASF para analizar los datos ASF. Si los datos ASF tienen longitudes de paquetes variables, debe establecer este atributo en los búferes multimedia que pase al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Establezca el atributo en **true** si el búfer contiene el inicio de un nuevo paquete. Si el búfer contiene una continuación del paquete anterior, establezca el atributo en **false**. Los búferes no pueden abarcar varios paquetes.

En el caso de los datos ASF con tamaños de paquete fijos, este atributo no es necesario y un búfer puede abarcar varios paquetes.

Tenga en cuenta que las implementaciones estándar de los [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) proporcionados por Media Foundation no exponen [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Para usar este atributo, debe proporcionar su propia implementación de **IMFMediaBuffer**; por ejemplo, ajustando los búferes devueltos por [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




