---
title: NAP Interfaces
description: NAP Interfaces
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161254"
---
# <a name="nap-interfaces"></a>NAP Interfaces

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP se compone de las interfaces siguientes.



| Nombre de la interfaz                                                                   | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Proporciona métodos que los usuarios de confianza de certificados deben usar para comunicarse con NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Se usa para la administración de clientes NAP de la caché de SoH y el desencadenador de intercambio de SoH. En desuso.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Se usa para la administración de clientes NAP de la caché de SoH y el desencadenador de intercambio de SoH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Se usa para la configuración personalizada de componentes shv. En desuso.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV) para configurar una interfaz de usuario del servidor de directivas de red (NPS) de forma remota.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Proporciona métodos de configuración del sistema NAP para validadores de estado del sistema (SHV) para establecer y modificar los datos de configuración de un identificador de configuración específico. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Debe implementarse mediante componentes de complemento, como SHA y SHV, para que el sistema NAP pueda comunicarse con ellos.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Lo usan los clientes de cumplimiento para comunicarse con NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Los clientes de cumplimiento deben implementar esta interfaz para permitir que NapAgent se comunique con ellos.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Permite la administración de conexiones de cliente. En desuso.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Permite la administración de conexiones de cliente.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Los SHV usan el método único en esta interfaz para indicar la finalización de solicitudes asincrónicas.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Lo usan los clientes de administración (por ejemplo, proveedores WMI, herramientas de línea de comandos, etc.) para consultar el estado del sistema de servidor NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Se usa para la administración básica del servidor NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Lo usan las SHA para construir solicitudes soH y shvs para construir respuestas soH.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Lo usan las SHA para procesar el contenido de las respuestas soH y los SHV para procesar el contenido de las solicitudes de SoH.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Las SHA deben usar esta interfaz para comunicarse con NapAgent. En desuso.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Las SHA deben usar esta interfaz para comunicarse con NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | Las SHA deben implementar esta interfaz para coordinar el procesamiento con el sistema NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | Las SHA usan esta interfaz para comunicarse y coordinar su procesamiento con el sistema NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Proporciona métodos que una SHV debe implementar para que el sistema NAP pueda comunicarse con él.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Los SHV usan esta interfaz para la comunicación de datos con su homólogo del lado cliente. En desuso.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Los SHV usan esta interfaz para la comunicación de datos con su homólogo del lado cliente.                                                                  |



 

 

 




