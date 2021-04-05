---
description: Configurar aplicaciones de biblioteca
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configurar aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51e00626d42044797881ccb86553ddfda38a089
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080147"
---
# <a name="configuring-library-applications"></a>Configurar aplicaciones de biblioteca

Dado que las aplicaciones de biblioteca COM+ se ejecutan en el proceso del cliente, los elementos configurables para las aplicaciones de biblioteca son considerablemente diferentes a los de las aplicaciones de servidor. No se puede configurar ningún aspecto de la aplicación que esté determinado por el proceso de hospedaje.

En el nivel de aplicación, varias configuraciones están limitadas o no están disponibles para las aplicaciones de biblioteca. Estas restricciones se describen en la tabla siguiente:



| Atributo                                       | Descripción                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de seguridad<br/>                       | Debe elegir comprobaciones de acceso de nivel de componente. La aplicación de biblioteca no puede influir en las comprobaciones de acceso de nivel de proceso. Consulte [configuración de un nivel de seguridad para las comprobaciones de acceso](setting-a-security-level-for-access-checks.md).<br/>             |
| Habilitación o deshabilitación de la autenticación<br/> | Puede indicar si la aplicación de biblioteca participará en la autenticación realizada por el proceso de host. Consulte [habilitación de la autenticación para una aplicación de biblioteca](enabling-authentication-for-a-library-application.md).<br/> |
| Nivel de suplantación<br/>                  | Dispone. Se usa la configuración del proceso de host. <br/>                                                                                                                                                                             |
| Identidad de seguridad<br/>                    | Dispone. La aplicación se ejecuta bajo la identidad del proceso de host.<br/>                                                                                                                                                          |
| Cierre de proceso de servidor<br/>              | Dispone.<br/>                                                                                                                                                                                                                       |
| Habilitar compatibilidad con 3 GB<br/>                  | Dispone.<br/>                                                                                                                                                                                                                       |
| Iniciar en el depurador<br/>                   | Dispone.<br/>                                                                                                                                                                                                                       |
| Habilitar CRM<br/>                           | Dispone.<br/>                                                                                                                                                                                                                       |
| MSMQ<br/>                              | Dispone.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de la aplicación COM+](com--application-overview.md)
</dt> </dl>

 

 




