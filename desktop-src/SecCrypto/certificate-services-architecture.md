---
description: Una plataforma de desarrollo para crear entidades de certificación para empresas o aplicaciones seguras de Internet.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Arquitectura de Servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d41a2dedb2ab576009a23f1a67417fb8230b4dfcc1d15629c2c9454469c734
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126884"
---
# <a name="certificate-services-architecture"></a>Arquitectura de Servicios de certificados

Certificate Services es una plataforma de desarrollo para crear entidades de certificación para empresas o aplicaciones seguras de Internet. Una entidad de certificación operativa y configurada permitirá que un sitio emita, realice un seguimiento, administre y revoque certificados con una sobrecarga de administración mínima y seguridad máxima.

Certificate Services consta del motor de servidor, la base de datos del servidor y un conjunto de módulos y herramientas que funcionan conjuntamente para funcionar como una entidad de certificación. Las aplicaciones externas, los módulos y las herramientas de administración usan interfaces del Modelo de objetos componentes (COM) para interactuar con el motor de servidor. En el diagrama siguiente se muestran las interfaces usadas por el motor de servidor:

![arquitectura de servicios de certificados](images/certapi.png)

Un sistema de certificación operativo normalmente tendrá cuatro subsistemas principales.



| Subsystem             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente                | El cliente es el software que usa el usuario final para generar una solicitud de [*certificado,*](../secgloss/c-gly.md)enviar la solicitud y recibir el certificado finalizado. Un ejemplo de cliente es Microsoft Internet Explorer versión 5. El cliente normalmente interactuará con una interfaz personalizada mantenida por la aplicación intermediaria.                                                                                                                                                                                                                                                                                              |
| Intermediario          | El intermediario es un subsistema que consta de la aplicación intermediaria y la interfaz de cliente de Servicios de certificados (cliente web de *Servicios* de certificados en el programa de instalación). La aplicación intermediaria interactúa directamente con el cliente, recibiendo solicitudes de certificado y devolviendo certificados terminados. Se comunica con el motor del servidor a través de la interfaz de cliente de Servicios de certificados, que contiene las interfaces [**COM ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) e [**ICertRequest.**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) Un ejemplo de una aplicación intermediaria es Microsoft Internet Information Services. La aplicación intermediaria se puede implementar completamente a través de Active Server Pages. |
| Servidor                | El servidor es el sistema que compila el certificado. Además del motor de servidor, se incluyen dos componentes configurables; el módulo de directivas y el módulo de salida. El módulo de directivas interactúa con el motor de servidor a través de las interfaces [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) [**e ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Los módulos de salida (puede haber más de uno) interactúan con el motor de servidor a través de las interfaces [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) [**e ICertServerExit.**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                                                                                                                                                                                       |
| Cliente administrativo | El cliente administrativo es el sistema que supervisa y administra certificados y solicitudes. El cliente administrativo usa la [**interfaz ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) para comunicarse con el motor del servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Para obtener más información sobre la arquitectura de Servicios de certificados, vea [Cryptography Interfaces](cryptography-interfaces.md), [Building a Certificate](building-a-certificate.md)y los temas siguientes.



| Sección                                      | Content                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Módulos de directivas](policy-modules.md)         | Programas personalizables que se pueden usar durante la evaluación de [*solicitudes de certificado*](../secgloss/c-gly.md); estos programas aplican las reglas por las que Certificate Services emite o deniega la solicitud. |
| [Salir de módulos](exit-modules.md)             | Programas personalizables que reciben notificaciones del motor de servidor cuando se producen operaciones, como cuando se emite un certificado.                                                                                                                                       |
| [Controladores de extensiones](extension-handlers.md) | Objetos COM que proporcionan rutinas para codificar las extensiones y los tipos de datos más complejos.                                                                                                                                                                                 |
| [Intermediarios](intermediaries.md)         | Programas que se comunican con las aplicaciones cliente para permitir el envío de solicitudes de certificado.                                                                                                                                                                        |



 

 

 
