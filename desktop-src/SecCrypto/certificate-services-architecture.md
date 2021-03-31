---
description: Plataforma de desarrollo para la creación de entidades de certificación para empresas o aplicaciones seguras de Internet.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Arquitectura de servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b7e0545b2f0fe0dd8c30d1863ffdf52c64a9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275663"
---
# <a name="certificate-services-architecture"></a>Arquitectura de servicios de certificados

Servicios de Certificate Server es una plataforma de desarrollo para la creación de entidades de certificación para empresas o aplicaciones seguras de Internet. Una entidad de certificación configurada y operativa permitirá a un sitio emitir, realizar un seguimiento, administrar y revocar certificados con una sobrecarga de administración mínima y una seguridad máxima.

Los servicios de Certificate Server se componen del motor del servidor, la base de datos del servidor y un conjunto de módulos y herramientas que funcionan conjuntamente para funcionar como una entidad de certificación. Las aplicaciones externas, los módulos y las herramientas de administración utilizan las interfaces del modelo de objetos componentes (COM) para interactuar con el motor del servidor. En el diagrama siguiente se muestran las interfaces utilizadas por el motor del servidor:

![arquitectura de servicios de certificados](images/certapi.png)

Normalmente, un sistema de certificación operativo tendrá cuatro subsistemas principales.



| Subsystem             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Remoto                | El cliente es el software que usa el usuario final para generar una solicitud de [*certificado*](../secgloss/c-gly.md), enviar la solicitud y recibir el certificado terminado. Un ejemplo de cliente es Microsoft Internet Explorer versión 5. Normalmente, el cliente interactuará con una interfaz personalizada mantenida por la aplicación intermediaria.                                                                                                                                                                                                                                                                                              |
| Intermediario          | El intermediario es un subsistema que consta de la aplicación intermediaria y la interfaz de cliente de servicios de Certificate Server (*cliente web de servicios de certificados* en el programa de instalación). La aplicación intermediaria interactúa directamente con el cliente, recibiendo solicitudes de certificado y devolviendo certificados finalizados. Se comunica con el motor de servidor a través de la interfaz de cliente de servicios de Certificate Server, que contiene las interfaces com [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) y [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) . Un ejemplo de una aplicación intermediaria es Microsoft Internet Information Services. La aplicación intermediaria se puede implementar completamente a través de Active Server páginas. |
| Servidor                | El servidor es el sistema que genera el certificado. Además del motor de servidor, se incluyen dos componentes configurables; el módulo de directivas y el módulo de salida. El módulo de directivas interactúa con el motor de servidor a través de las interfaces [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) y [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Los módulos de salida (puede haber más de uno) interactuar con el motor de servidor a través de las interfaces [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) y [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) .                                                                                                                                                                                       |
| Cliente administrativo | El cliente administrativo es el sistema que supervisa y administra los certificados y las solicitudes. El cliente administrativo usa la interfaz [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) para comunicarse con el motor de servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Para obtener más información acerca de la arquitectura de servicios de certificados, vea [interfaces criptográficas](cryptography-interfaces.md), [crear un certificado](building-a-certificate.md)y los temas siguientes.



| Sección                                      | Contenido                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Módulos de directivas](policy-modules.md)         | Programas personalizables que se pueden usar durante la evaluación de [*solicitudes de certificado*](../secgloss/c-gly.md); Estos programas aplican las reglas por las que los servicios de Certificate Server emiten o deniegan la solicitud. |
| [Módulos de salida](exit-modules.md)             | Programas personalizables que reciben notificaciones del motor de servidor cuando se producen las operaciones, como cuando se emite un certificado.                                                                                                                                       |
| [Controladores de extensión](extension-handlers.md) | Objetos COM que proporcionan rutinas para codificar las extensiones y tipos de datos más complejos.                                                                                                                                                                                 |
| [Media](intermediaries.md)         | Programas que se comunican con las aplicaciones cliente para permitir el envío de solicitudes de certificado.                                                                                                                                                                        |



 

 

 
