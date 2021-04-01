---
description: Especifica el estado de un intento de resolver una topología.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908455"
---
# <a name="mf_topology_resolution_status-attribute"></a>Atributo de estado de resolución de \_ topología MF \_ \_

Especifica el estado de un intento de resolver una topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El cargador de topologías o la sesión multimedia podrían establecer este atributo en una topología. El valor de este atributo es **una operación OR** bit a bit de marcas de la enumeración de [**marcas de estado de \_ resolución de topología \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




