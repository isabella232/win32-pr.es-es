---
description: Configuración de aplicaciones de biblioteca
ms.assetid: db375e0f-74ca-44df-918a-b0e48742a594
title: Configuración de aplicaciones de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ea0018d74070828384db25d76c73e7b5b3dba8a7dfc7d091c94e38aa0c3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047503"
---
# <a name="configuring-library-applications"></a>Configuración de aplicaciones de biblioteca

Dado que las aplicaciones de biblioteca COM+ se ejecutan en el proceso del cliente, los elementos configurables para las aplicaciones de biblioteca son considerablemente diferentes que para las aplicaciones de servidor. No puede configurar ningún aspecto de la aplicación determinado por el proceso de hospedaje.

En el nivel de aplicación, hay varias opciones de configuración limitadas o no disponibles para las aplicaciones de biblioteca. Estas restricciones se describen en la tabla siguiente:



| Atributo                                       | Descripción                                                                                                                                                                                                                                   |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nivel de seguridad<br/>                       | Debe elegir comprobaciones de acceso de nivel de componente. La aplicación de biblioteca no puede influir en las comprobaciones de acceso de nivel de proceso. Vea [Establecer un nivel de seguridad para las comprobaciones de acceso.](setting-a-security-level-for-access-checks.md)<br/>             |
| Habilitación o deshabilitación de la autenticación<br/> | Puede indicar si la aplicación de biblioteca participará en la autenticación realizada por el proceso de host. Consulte [Habilitación de la autenticación para una aplicación de biblioteca.](enabling-authentication-for-a-library-application.md)<br/> |
| Nivel de suplantación<br/>                  | Carácter. Se usa la configuración del proceso de host. <br/>                                                                                                                                                                             |
| Identidad de seguridad<br/>                    | Carácter. La aplicación se ejecuta bajo la identidad del proceso de host.<br/>                                                                                                                                                          |
| Apagado del proceso del servidor<br/>              | Carácter.<br/>                                                                                                                                                                                                                       |
| Habilitación de la compatibilidad con 3 GB<br/>                  | Carácter.<br/>                                                                                                                                                                                                                       |
| Inicio en el depurador<br/>                   | Carácter.<br/>                                                                                                                                                                                                                       |
| Habilitación de CRM<br/>                           | Carácter.<br/>                                                                                                                                                                                                                       |
| Cola<br/>                              | Carácter.<br/>                                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a la aplicación COM+](com--application-overview.md)
</dt> </dl>

 

 




