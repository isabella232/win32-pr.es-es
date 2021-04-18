---
description: Explica cómo crear paquetes de seguridad personalizados mediante la API del paquete de seguridad personalizado.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Paquetes de seguridad personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4c447f1a24a3edc2f25a55f83d82c174094c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652455"
---
# <a name="custom-security-packages"></a>Paquetes de seguridad personalizados

Para implementar nuevos protocolos de seguridad que se integren con los sistemas operativos Windows Server y Windows, use la API del paquete de seguridad personalizado y las funciones de la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA).

La API del paquete de seguridad personalizado admite el desarrollo combinado de [*proveedores de compatibilidad para seguridad*](/windows/desktop/SecGloss/s-gly) (SSP) personalizados, que proporcionan servicios de [autenticación no interactivos](noninteractive-authentication.md) y un intercambio de mensajes seguro a aplicaciones cliente/servidor, con el desarrollo de [*paquetes de autenticación*](/windows/desktop/SecGloss/a-gly)personalizados, que proporcionan servicios para aplicaciones que realizan la [autenticación interactiva](interactive-authentication.md). Estos servicios, cuando se combinan en un único paquete, reciben el nombre de proveedor de compatibilidad para seguridad/paquete de autenticación (SSP/AP).

Al igual que con los paquetes de seguridad proporcionados por Microsoft, los usuarios del paquete de seguridad personalizado acceden a los servicios de autenticación interactiva mediante las [funciones de inicio de sesión LSA](authentication-functions.md). Se puede tener acceso directo a los servicios de autenticación y protección de mensajes no interactivos mediante la [interfaz del proveedor de compatibilidad para seguridad](sspi.md) (SSPI).

Los paquetes de seguridad implementados en SSP/APs están totalmente integrados con la LSA. Con las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad personalizados, los desarrolladores pueden implementar características de seguridad avanzadas, como la creación de tokens, la compatibilidad con [*credenciales adicionales*](/windows/desktop/SecGloss/s-gly) y la autenticación de paso a través. Para obtener una lista de estas funciones de soporte técnico, consulte [funciones de LSA llamadas por paquetes de autenticación](authentication-functions.md). Para obtener información sobre cómo implementar paquetes de seguridad personalizados, vea [crear paquetes de seguridad personalizados](creating-custom-security-packages.md).

Para obtener más información acerca de los paquetes de seguridad personalizados, vea los temas siguientes.



| Tema                                                                                                                                                 | Descripción                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APs frente a SSP](ssp-aps-versus-ssps.md)<br/>                                                                                                | Información sobre cómo determinar si un paquete de seguridad debe estar en un SSP/AP o SSP.<br/> |
| [Modo LSA frente al modo usuario](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Detalles sobre cómo el modo LSA y el modo de usuario son diferentes.<br/>                                      |
| [Restricciones en relación con el registro y la instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Acciones por paquetes de seguridad que no se admiten en Windows.<br/>                              |



 

 

