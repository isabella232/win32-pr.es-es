---
title: Compatibilidad con bits de estado varios
description: Compatibilidad con bits de estado varios
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096925"
---
# <a name="miscellaneous-status-bits-support"></a>Compatibilidad con bits de estado varios

ActiveX Los contenedores de controles deben reconocer y admitir los siguientes bits de estado \_ OLEMISC.



| Bit de estado                           | ¿Necesario?      | Comentarios                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necesario para la compatibilidad con controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE es para contenedores que hospedan controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE se introduce como parte de la especificación ActiveX Controls 96, consulte esta documentación para obtener más detalles.<br/> |
| Insideout<br/>                 | No<br/>  | Normalmente no se usa con ActiveX, sino con incrustaciones de documentos compuestos. Tenga en cuenta que esto es contrario a alguna documentación del SDK que indica que este bit debe establecerse para que se establezca el bit ACTIVATEWHENVISIBLE.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sí<br/> | Designa un control que debe ser visible en tiempo de diseño, pero invisible en tiempo de ejecución.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | Normalmente, la compatibilidad es obligatoria, aunque no es necesaria para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | Normalmente, la compatibilidad es obligatoria, aunque no es necesaria para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ALIGNABLE<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Consulte [Contención del sitio de marco simple](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | Se recomienda la compatibilidad con este bit, pero no es obligatoria.<br/>                                                                                                                                                                                                                                       |
| Imemode<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 





