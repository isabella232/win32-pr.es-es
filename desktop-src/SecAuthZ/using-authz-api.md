---
description: Authz API permite a las aplicaciones realizar comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que los Access Control de bajo nivel.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Uso de la API de authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361540"
---
# <a name="using-authz-api"></a>Uso de la API de authz

Authz API permite a las aplicaciones realizar comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que los [Access Control de bajo nivel](low-level-access-control.md).

Authz API permite a las aplicaciones almacenar en caché las comprobaciones de acceso para mejorar el rendimiento, consultar y modificar contextos de cliente, y definir reglas de negocios que se pueden usar para evaluar dinámicamente el permiso de acceso.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                             | Descripción                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Inicializar un contexto de cliente](initializing-a-client-context.md)<br/>     | Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.<br/>                                                                                                                                            |
| [Consultar un contexto de cliente](querying-a-client-context.md)<br/>             | Las aplicaciones pueden llamar a la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar información sobre un contexto de cliente existente.<br/>                                                                                       |
| [Agregar SID a un contexto de cliente](adding-sids-to-a-client-context.md)<br/> | Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente llamando a la función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .<br/> |
| [Comprobación del acceso con la API de authz](checking-access-with-authz-api.md)<br/>   | Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .<br/>                                                                                                                |
| [Almacenar en caché comprobaciones de acceso](caching-access-checks.md)<br/>                     | Cuando una aplicación realiza una comprobación de acceso mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , los resultados de esa comprobación de acceso se pueden almacenar en caché.<br/>                                                                                       |



 

 

