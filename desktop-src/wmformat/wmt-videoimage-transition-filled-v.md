---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl.h)
description: La transición rellena de V revela la nueva imagen en un triángulo que se origina en un lado del marco.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466162"
---
# <a name="wmt_videoimage_transition_filled_v"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V

La transición rellena de V revela la nueva imagen en un triángulo que se origina en un lado del marco.

## <a name="parameters"></a>Parámetros

En la tabla siguiente se describen los parámetros utilizados por esta transición y se enumeran los miembros de la estructura [**\_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) de WMT a la que están asignados.




| Parámetro | Miembro de estructura | Description | 
|-----------|------------------|-------------|
| Ancho | <strong>fEffectPara0</strong> | Ancho de la V rellena en píxeles. | 
| Alto | <strong>fEffectPara1</strong> | Alto de la V rellena en píxeles. | 
| Dirección | <strong>fEffectPara2</strong> | Dirección desde la que se origina la V rellena. Establezca en uno de los siguientes valores:<br /><ul><li>0: escribe desde el lado izquierdo del marco.</li><li>1 : escribe desde el lado derecho del marco.</li><li>2 - Escribe desde la parte inferior del marco.</li><li>3 - Escribe desde la parte superior del marco.</li></ul> | 
| Composición | <strong>fEffectPara3</strong> | Establezca en uno de los siguientes valores:<ul><li>0: especifica la composición normal, en la que la imagen anterior es el fondo y la imagen actual es el primer plano.</li><li>1 - Especifica la composición invertida, en la que la imagen actual es la imagen de fondo, y la imagen anterior es el primer plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Transiciones de imágenes de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





