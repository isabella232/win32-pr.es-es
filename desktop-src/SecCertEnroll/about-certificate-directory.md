---
description: Una infraestructura de clave pública (PKI) de Windows guarda los certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directorio de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279472"
---
# <a name="certificate-directory"></a>Directorio de certificados

Una infraestructura de clave pública (PKI) de Windows guarda los certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local. Normalmente, el almacenamiento de CA se conoce como la base de datos de certificados y el almacenamiento local se conoce como el almacén de certificados.

## <a name="certificate-database"></a>Base de datos de certificados

Al agregar servicios de servidor de certificados en un servidor de Windows y configurar una CA, se crea una base de datos de certificados. De forma predeterminada, la base de datos se encuentra en la carpeta *% systemroot%* \\ system32 \\ Certlog y el nombre se basa en el nombre de la entidad de certificación con una extensión. edb. La base de datos puede contener:

-   Certificados emitidos
-   Certificados revocados
-   Claves privadas archivadas
-   Solicitudes de certificado

No se puede usar la API de inscripción de certificados para manipular la base de datos. El proceso de inscripción crea automáticamente las entradas necesarias.

## <a name="certificate-stores"></a>Almacenes de certificados

Servicios de certificados de Microsoft copia los certificados emitidos y las solicitudes pendientes o rechazadas a los equipos y dispositivos locales. La ubicación de almacenamiento se denomina almacén de certificados y consta de los siguientes almacenes lógicos.

| Almacén lógico                                         | Descripción                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Personal<br/>                                   | Contiene certificados asociados a una clave privada controlada por el usuario o el equipo.<br/>                     |
| Entidades de certificación raíz de confianza<br/>     | Contiene certificados de entidades de certificación (CA) de confianza implícita.<br/>                              |
| Confianza empresarial<br/>                           | Contiene listas de certificados de confianza que se suelen usar para confiar en los certificados autofirmados de otras organizaciones.<br/> |
| Entidades de certificación intermedias<br/>     | Contiene certificados emitidos para entidades de certificación subordinadas en la jerarquía de certificados.<br/>                             |
| Objeto de usuario de Active Directory<br/>               | Contiene el certificado de objeto de usuario o los certificados publicados en Active Directory.<br/>                         |
| Publicadores de confianza<br/>                         | Contiene certificados de entidades de certificación de confianza.<br/>                                                                     |
| Certificados que no son de confianza<br/>                     | Contiene certificados que se han identificado explícitamente como que no son de confianza.<br/>                                    |
| Entidades de certificación raíz de tercero<br/> | Contiene certificados raíz de confianza de entidades de certificación fuera de la jerarquía interna de certificados.<br/>                     |
| Personas de confianza<br/>                             | Contiene certificados emitidos para usuarios o entidades de confianza explícita.<br/>                        |
| Otras personas<br/>                               | Contiene certificados emitidos para usuarios o entidades de confianza implícita.<br/>                        |
| Solicitudes de inscripción de certificado<br/>            | Contiene solicitudes de certificados pendientes o rechazadas.<br/>                                                          |



 

No se puede usar la API de inscripción de certificados para especificar o recuperar propiedades de almacén o para copiar certificados en almacenes específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 




