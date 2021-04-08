---
title: Cómo funciona Access Control en Active Directory Domain Services
description: El control de acceso para los objetos de Active Directory Domain Services se basa en los modelos de control de acceso de Windows NT y Windows 2000.
ms.assetid: 70eed84b-ada0-48e7-b448-704586e9afaa
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, seguridad, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2893c068e5a841ed609808964f203211309eaf4f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995079"
---
# <a name="how-access-control-works-in-active-directory-domain-services"></a>Cómo funciona Access Control en Active Directory Domain Services

El control de acceso para los objetos de Active Directory Domain Services se basa en los modelos de control de acceso de Windows NT y Windows 2000. Para obtener más información y una descripción detallada de este modelo y sus componentes, como descriptores de seguridad, tokens de acceso, SID, ACL y ACE, vea [modelo de Access Control](/windows/desktop/SecAuthZ/access-control-model).

Los privilegios de acceso para los recursos de Active Directory Domain Services se conceden normalmente mediante el uso de una entrada de control de acceso (ACE). Una ACE define un permiso de acceso o auditoría en un objeto para un usuario o grupo específico. Una lista de control de acceso (ACL) es la colección ordenada de entradas de control de acceso definidas para un objeto. Un descriptor de seguridad admite propiedades y métodos que crean y administran las ACL. Para obtener más información acerca de los modelos de seguridad, vea [Security (seguridad](/windows/desktop/SecAuthZ/access-control) ) o el kit de recursos del *servidor de Windows 2000*. (Es posible que este recurso no esté disponible en algunos idiomas y países o regiones).

El esquema básico del modelo de seguridad es:

-   Descriptor de seguridad. Cada objeto de directorio tiene su propio descriptor de seguridad que contiene los datos de seguridad que protegen el objeto. El descriptor de seguridad puede contener una lista de control de acceso discrecional (DACL). Una DACL contiene una lista de ACE. Cada ACE concede o deniega un conjunto de derechos de acceso a un usuario o grupo. Los derechos de acceso se corresponden con las operaciones, como la lectura y la escritura de propiedades, que se pueden realizar en el objeto.
-   Contexto de seguridad. Cuando se tiene acceso a un objeto de directorio, la aplicación especifica las credenciales de la entidad de seguridad que está realizando el intento de acceso. Cuando se autentica, estas credenciales determinan el contexto de seguridad de la aplicación, que incluye las pertenencias a grupos y los privilegios asociados a la entidad de seguridad. Para obtener más información sobre los contextos de seguridad, vea [contextos de seguridad y Active Directory Domain Services](security-contexts-and-active-directory-domain-services.md).
-   Comprobación de acceso. El sistema concede acceso a un objeto solo si el descriptor de seguridad del objeto concede los derechos de acceso necesarios a la entidad de seguridad que intenta la operación (o a los grupos a los que pertenece la entidad de seguridad).

En la tabla siguiente se enumeran las interfaces ADSI utilizadas para manipular las características de control de acceso de Active Directory Domain Services.



| Interfaz                                                 | Descripción                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------|
| [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) | Se utiliza para leer y escribir las propiedades de seguridad de un objeto de servicio de directorio. |
| [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)   | Se utiliza para administrar y enumerar todas las ACE para un objeto de servicio de directorio.     |
| [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) | Se usa para leer y escribir propiedades ACE.                                    |



 

 

 