---
description: Una Windows de clave pública (PKI) guarda certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directorio de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b77a7c63e234460394005aac416d41ff7845470139ba2cb8b700132bea0118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904834"
---
# <a name="certificate-directory"></a>Directorio de certificados

Una Windows de clave pública (PKI) guarda certificados en el servidor que hospeda la entidad de certificación (CA) y en el equipo o dispositivo local. El almacenamiento de ca se conoce normalmente como la base de datos de certificados y el almacenamiento local se conoce como almacén de certificados.

## <a name="certificate-database"></a>Base de datos de certificados

Al agregar Servicios de certificados en un servidor Windows y configurar una entidad de certificación, se crea una base de datos de certificados. De forma predeterminada, la base de datos se encuentra en la carpeta *%SystemRoot%* System32 Certlog y el nombre se basa en el nombre de la entidad de certificación con una \\ \\ extensión .edb. La base de datos puede contener:

-   Certificados emitidos
-   Certificados revocados
-   Claves privadas archivadas
-   Solicitudes de certificado

No puede usar la API de inscripción de certificados para manipular la base de datos. El proceso de inscripción crea automáticamente las entradas necesarias.

## <a name="certificate-stores"></a>Almacenes de certificados

Microsoft Certificate Services copia los certificados emitidos y las solicitudes pendientes o rechazadas a equipos y dispositivos locales. La ubicación de almacenamiento se denomina almacén de certificados y consta de los siguientes almacenes lógicos.

| Almacén lógico                                         | Descripción                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Personal<br/>                                   | Contiene certificados asociados a una clave privada controlada por el usuario o el equipo.<br/>                     |
| Entidades de certificación raíz de confianza<br/>     | Contiene certificados de entidades de certificación (CA) de confianza implícita.<br/>                              |
| Confianza empresarial<br/>                           | Contiene listas de confianza de certificados que se usan normalmente para confiar en certificados autofirmados de otras organizaciones.<br/> |
| Entidades de certificación intermedias<br/>     | Contiene certificados emitidos para entidades de certificación subordinadas en la jerarquía de certificados.<br/>                             |
| Objeto de usuario de Active Directory<br/>               | Contiene el certificado de objeto de usuario o los certificados publicados en Active Directory.<br/>                         |
| Publicadores de confianza<br/>                         | Contiene certificados de entidades de certificación de confianza.<br/>                                                                     |
| Certificados que no son de confianza<br/>                     | Contiene certificados que se han identificado explícitamente como no de confianza.<br/>                                    |
| Entidades de certificación raíz de tercero<br/> | Contiene certificados raíz de confianza de ca fuera de la jerarquía de certificados interna.<br/>                     |
| Personas de confianza<br/>                             | Contiene certificados emitidos para usuarios o entidades de confianza explícita.<br/>                        |
| Otras personas<br/>                               | Contiene certificados emitidos para usuarios o entidades de confianza implícita.<br/>                        |
| Solicitudes de inscripción de certificado<br/>            | Contiene solicitudes de certificado pendientes o rechazadas.<br/>                                                          |



 

No puede usar la API de inscripción de certificados para especificar o recuperar las propiedades del almacén ni copiar certificados en almacenes específicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos PKI](about-pki-components.md)
</dt> </dl>

 

 




