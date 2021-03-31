---
title: Compatibilidad con bits de estado varios
description: Compatibilidad con bits de estado varios
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075042"
---
# <a name="miscellaneous-status-bits-support"></a>Compatibilidad con bits de estado varios

Los contenedores de controles ActiveX deben reconocer y admitir los siguientes bits de estado de OLEMISC \_ .



| Bit de estado                           | ¿Necesario?      | Comentarios                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necesario para la compatibilidad con controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE es para contenedores que hospedan controles inactivos y sin ventanas. El bit IGNOREACTIVATEWHENVISIBLE se incluye como parte de la especificación de los controles ActiveX 96, consulte esta documentación para obtener más detalles.<br/> |
| INSIDEOUT<br/>                 | No<br/>  | No se utiliza normalmente con controles ActiveX, sino con incrustaciones de documentos compuestos. Tenga en cuenta que esto es contrario a la documentación del SDK que indica que este bit debe establecerse para que se establezca el bit ACTIVATEWHENVISIBLE.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sí<br/> | Designa un control que debe ser visible en tiempo de diseño, pero invisible en tiempo de ejecución.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | La compatibilidad es normalmente obligatoria, aunque no es necesario para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | La compatibilidad es normalmente obligatoria, aunque no es necesario para los contenedores de estilo de documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sí<br/> |                                                                                                                                                                                                                                                                                                         |
| ALINEAble<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Vea [contención de sitio de marco simple](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | Se recomienda la compatibilidad con este bit, pero no es obligatorio.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contenedores](containers.md)
</dt> </dl>

 

 





