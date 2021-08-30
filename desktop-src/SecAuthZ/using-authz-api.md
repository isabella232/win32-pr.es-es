---
description: Authz API permite que las aplicaciones realicen comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que las aplicaciones de Access Control.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Uso de Authz API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58ec0f22b8818a9d9a04a3d75a53bba161e55c8292212096b8d7fb7816df3363
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960765"
---
# <a name="using-authz-api"></a>Uso de Authz API

Authz API permite a las aplicaciones realizar comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que los de [bajo Access Control](low-level-access-control.md).

Authz API permite a las aplicaciones almacenar en caché las comprobaciones de acceso para mejorar el rendimiento, consultar y modificar contextos de cliente y definir reglas de negocios que se pueden usar para evaluar el permiso de acceso dinámicamente.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                             | Descripción                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializar un contexto de cliente](initializing-a-client-context.md)<br/>     | Una aplicación debe crear un contexto de cliente para poder usar Authz API para realizar comprobaciones de acceso o auditoría.<br/>                                                                                                                                            |
| [Consulta de un contexto de cliente](querying-a-client-context.md)<br/>             | Las aplicaciones pueden llamar a [**la función AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar información sobre un contexto de cliente existente.<br/>                                                                                       |
| [Agregar SID a un contexto de cliente](adding-sids-to-a-client-context.md)<br/> | Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente llamando a la función [**AuthzAddSidsToContext.**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext)<br/> |
| [Comprobación del acceso con Authz API](checking-access-with-authz-api.md)<br/>   | Las aplicaciones determinan si se debe conceder acceso a objetos protegibles mediante una llamada a la [**función AuthzAccessCheck.**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)<br/>                                                                                                                |
| [Almacenamiento en caché de comprobaciones de acceso](caching-access-checks.md)<br/>                     | Cuando una aplicación realiza una comprobación de acceso mediante una llamada a la función [**AuthzAccessCheck,**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) los resultados de esa comprobación de acceso se pueden almacenar en caché.<br/>                                                                                       |



 

 

