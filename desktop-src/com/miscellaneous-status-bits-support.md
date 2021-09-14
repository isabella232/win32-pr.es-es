---
title: Compatibilidad con bits de estado varios
description: Compatibilidad con bits de estado varios
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889025"
---
# <a name="miscellaneous-status-bits-support"></a>Compatibilidad con bits de estado varios

ActiveX Los contenedores de controles deben reconocer y admitir los siguientes bits de \_ estado OLEMISC.



| Bit de estado                           | ¿Necesario?      | Comentarios                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necesario para la compatibilidad con controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE es para contenedores que hospedan controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE se introduce como parte de la especificación ActiveX Controls 96; consulte esta documentación para obtener más detalles.<br/> |
| INSIDEOUT<br/>                 | No<br/>  | No suele usarse con controles ActiveX, sino con incrustaciones de documentos compuestas. Tenga en cuenta que esto es contrario a alguna documentación del SDK que dice que este bit debe establecerse para que se establezca el bit ACTIVATEWHENVISIBLE.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sí<br/> | Designa un control que debe ser visible en tiempo de diseño, pero invisible en tiempo de ejecución.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | Normalmente, la compatibilidad es obligatoria, aunque no es necesaria para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | Normalmente, la compatibilidad es obligatoria, aunque no es necesaria para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ALIGNABLE<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Consulte [Contención del sitio de marco simple](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | Se recomienda la compatibilidad con este bit, pero no es obligatoria.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 





