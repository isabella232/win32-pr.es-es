---
description: Explica cómo crear paquetes de seguridad personalizados mediante la API de paquete de seguridad personalizada.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Paquetes de seguridad personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799edb3eb8e0551afe7d7f7bcdc54924228445d6ffb28cb4773af843b5c2d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008673"
---
# <a name="custom-security-packages"></a>Paquetes de seguridad personalizados

Para implementar nuevos protocolos de seguridad integrados con los sistemas operativos Windows Server y Windows, use la API de paquete de seguridad personalizada y las funciones de autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA).

La API de paquetes de seguridad personalizados admite el [](noninteractive-authentication.md) desarrollo combinado de proveedores de compatibilidad de seguridad [*personalizados*](/windows/desktop/SecGloss/s-gly) (SSP), que proporcionan servicios de autenticación no interactiva e intercambio seguro de mensajes a aplicaciones cliente/servidor, con el desarrollo de paquetes de autenticación personalizados, [](/windows/desktop/SecGloss/a-gly)que proporcionan servicios para las aplicaciones que realizan la autenticación [interactiva.](interactive-authentication.md) Estos servicios, cuando se combinan en un único paquete, se denominan proveedor de compatibilidad de seguridad/paquete de autenticación (SSP/AP).

Al igual que con los paquetes de seguridad proporcionados por Microsoft, los usuarios del paquete de seguridad personalizado acceden a los servicios de autenticación interactiva mediante las funciones de [inicio de sesión de LSA](authentication-functions.md). Se puede acceder a los servicios de autenticación no activa y protección de mensajes directamente mediante [la interfaz](sspi.md) del proveedor de soporte técnico de seguridad (SSPI).

Los paquetes de seguridad implementados en SSP/AP están totalmente integrados con el LSA. Con las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad personalizados, los desarrolladores pueden implementar características de seguridad avanzadas, como la creación de [*tokens,*](/windows/desktop/SecGloss/s-gly) la compatibilidad con credenciales complementarias y la autenticación de paso a través. Para obtener una lista de estas funciones de compatibilidad, vea [Funciones LSA llamadas por paquetes de autenticación](authentication-functions.md). Para obtener información sobre cómo implementar paquetes de seguridad personalizados, vea [Crear paquetes de seguridad personalizados.](creating-custom-security-packages.md)

Para obtener más información sobre los paquetes de seguridad personalizados, vea los temas siguientes.



| Tema                                                                                                                                                 | Descripción                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/AP frente a SSP](ssp-aps-versus-ssps.md)<br/>                                                                                                | Información sobre cómo determinar si un paquete de seguridad debe estar en un SSP/AP o SSP.<br/> |
| [Modo LSA frente al modo de usuario](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Detalles sobre cómo el modo LSA y el modo de usuario son diferentes.<br/>                                      |
| [Restricciones en torno al registro e instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Acciones de paquetes de seguridad que no se admiten en Windows.<br/>                              |



 

 

