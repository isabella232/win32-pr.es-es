---
description: Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: MF_TOPONODE_DISABLE_PREROLL atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649239"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>MF \_ TOPONODE \_ deshabilitar \_ atributo de preroll

Especifica si la sesión multimedia utiliza el preparado en el receptor de medios representado por este nodo de topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de salida (**\_ nodo de \_ salida \_ de topología MF**).

Si el valor de este atributo es **true**, la sesión multimedia no revierte los datos en el receptor de medios, aunque el receptor de medios exponga la interfaz [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) . Si el valor es **false**, la sesión multimedia preprocesa los datos si el receptor multimedia implementa **IMFMediaSinkPreroll**. El valor predeterminado es **FALSE**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> </dl>

 

 




