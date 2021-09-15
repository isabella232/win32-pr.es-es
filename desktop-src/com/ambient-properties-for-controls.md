---
title: Propiedades ambientales para controles
description: Propiedades ambientales para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574145"
---
# <a name="ambient-properties-for-controls"></a>Propiedades ambientales para controles

Si un control admite propiedades ambientales, al menos debe respetar los valores de las siguientes propiedades ambientales en las condiciones indicadas en la tabla siguiente mediante el estándar dispids.



| Propiedad Ambient            | Desaconsulte          | Comentario o condiciones de uso                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Si la configuración regional es significativa para el control, por ejemplo, para la salida de texto<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | Si el control se comporta de forma diferente en modo de usuario (diseño) y modo de ejecución<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Si el control reacciona a los eventos de la interfaz de usuario, debe respetar esta propiedad de ambiente.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Si el control admite el redimensionamiento local de sí mismo<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Si el control admite la activación local y la activación de la interfaz de usuario<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Solo si el control está marcado como OLEMISC ACTSLIKEBUTTON (lo que significa que se proporciona compatibilidad con teclas mnemotécnicas de teclado, por lo tanto, se deben implementar \_ [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic).**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> |



 

Como se ha descrito anteriormente, el uso de ambientes requiere [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como mínimo) así como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) y [**GetClientSite).**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)

Es posible que el bit SETCLIENTSITEFIRST OLEMISC no sea \_ necesariamente compatible con un contenedor. En estas circunstancias, un control debe recurrir a los valores predeterminados para las propiedades ambientales que requiere.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





