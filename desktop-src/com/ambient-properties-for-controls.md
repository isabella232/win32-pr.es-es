---
title: Propiedades ambientales para controles
description: Propiedades ambientales para controles
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421a643873e818d8f5c0e006b4bb9049c1230c5f4e18525cdf7ed2b4175797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994065"
---
# <a name="ambient-properties-for-controls"></a>Propiedades ambientales para controles

Si un control admite propiedades ambientales, al menos debe respetar los valores de las siguientes propiedades ambientales en las condiciones indicadas en la tabla siguiente mediante el estándar dispids.



| Propiedad Ambient            | Despid          | Comentario/Condiciones de uso                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Si la configuración regional es significativa para el control, por ejemplo, para la salida de texto<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | Si el control se comporta de forma diferente en modo de usuario (diseño) y modo de ejecución<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Si el control reacciona a los eventos de la interfaz de usuario, debe respetar esta propiedad de ambiente.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Si el control admite el redimensionamiento en su lugar de sí mismo<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Si el control admite la activación en contexto y la activación de la interfaz de usuario<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Solo si el control está marcado como OLEMISC ACTSLIKEBUTTON (lo que significa que se proporciona compatibilidad con teclas de teclado, por lo tanto, se deben implementar \_ [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic).**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> |



 

Como se ha descrito anteriormente, el uso de ambientes requiere [**tanto IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (para [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) como mínimo) como [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (para [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) y [**GetClientSite).**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)

Es posible que el bit SETCLIENTSITEFIRST de OLEMISC \_ no sea necesariamente compatible con un contenedor. En estas circunstancias, un control debe recurrir a los valores predeterminados para las propiedades ambientales que requiere.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 





