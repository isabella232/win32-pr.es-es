---
title: Interfaces NAP
description: Interfaces NAP
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076232"
---
# <a name="nap-interfaces"></a>Interfaces NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP se compone de las siguientes interfaces.



| Nombre de la interfaz                                                                   | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Proporciona métodos que los usuarios de confianza de certificados deben usar para comunicarse con el NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Se usa para la administración del cliente NAP de la caché de SoH y el desencadenador de intercambio de SoH. En desuso.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Se usa para la administración del cliente NAP de la caché de SoH y el desencadenador de intercambio de SoH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Se usa para la configuración personalizada de los componentes de SHV. En desuso.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Proporciona métodos de configuración del sistema NAP para validadores de mantenimiento del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de redes (NPS) de forma remota.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Proporciona métodos de configuración del sistema NAP para que los validadores de mantenimiento del sistema (SHV) establezcan y modifiquen los datos de configuración de un identificador de configuración específico. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Debe implementarse mediante componentes de complemento, como Sha y SHV, para que el sistema NAP pueda comunicarse con ellos.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Lo usan los clientes de cumplimiento para comunicarse con el NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Los clientes de cumplimiento deben implementar esta interfaz para permitir que NapAgent se comunique con ellas.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Permite la administración de conexiones de cliente. En desuso.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Permite la administración de conexiones de cliente.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Los SHV usan el método único en esta interfaz para indicar la finalización de la solicitud asincrónica.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Lo usan los clientes de administración (por ejemplo, proveedores de WMI, herramientas de línea de comandos, etc.) para consultar el estado del sistema del servidor NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Se usa para la administración básica del servidor NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Lo usan los Sha para construir solicitudes de SoH y por SHV para construir respuestas de SoH.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Lo usan los Sha para procesar el contenido de las respuestas de SoH y de los SHV para procesar el contenido de las solicitudes de SoH.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Los Sha deben utilizar esta interfaz para comunicarse con el NapAgent. En desuso.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Los Sha deben utilizar esta interfaz para comunicarse con el NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | Sha debe implementar esta interfaz para coordinar el procesamiento con el sistema NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | Sha use esta interfaz para comunicarse y coordinar su procesamiento con el sistema NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Proporciona métodos que un SHV debe implementar para que el sistema NAP pueda comunicarse con él.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Los SHV usan esta interfaz para la comunicación de datos con el homólogo del lado cliente. En desuso.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Los SHV usan esta interfaz para la comunicación de datos con el homólogo del lado cliente.                                                                  |



 

 

 




