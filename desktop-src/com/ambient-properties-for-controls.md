---
title: Propiedades de ambiente para controles
description: Propiedades de ambiente para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418823"
---
# <a name="ambient-properties-for-controls"></a>Propiedades de ambiente para controles

Si un control admite cualquier propiedad de ambiente, debe respetar al menos los valores de las siguientes propiedades de ambiente en las condiciones indicadas en la siguiente tabla con los DISPID estándar.



| Propiedad Ambient            | DISPID          | Comentario y condiciones para su uso                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Si la configuración regional es significativa para el control, por ejemplo, para la salida de texto<br/>                                                                                                                                                                                                                  |
| En modo usuario <br/>        | -709<br/> | Si el control se comporta de forma diferente en modo de usuario (diseño) y modo de ejecución<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Si el control reacciona a los eventos de la interfaz de usuario, debe respetar esta propiedad de ambiente<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Si el control admite el cambio de tamaño en contexto de sí mismo<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Si el control admite la activación en contexto y la activación de la interfaz de usuario<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Solo si el control está marcado como OLEMISC \_ ACTSLIKEBUTTON (lo que significa que se proporciona compatibilidad con teclas de método abreviado, por lo que se debe implementar [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) y [**IOleControl::**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) ).<br/> |



 

Tal y como se ha descrito anteriormente, el uso de los ambiente requiere [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como mínimo), así como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) y [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).

\_Es posible que un contenedor no admita necesariamente el bit OLEMISC SETCLIENTSITEFIRST. En estas circunstancias, un control debe recurrir a los valores predeterminados para las propiedades de ambiente que requiere.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





