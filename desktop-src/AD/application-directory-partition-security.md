---
title: Seguridad de partición de directorio de aplicaciones
description: El modelo de control de acceso y seguridad para las particiones de directorio de aplicación es el mismo que el de otras particiones en Active Directory Domain Services.
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- AD de seguridad de partición de directorio de aplicaciones
- Particiones de directorio de aplicaciones (AD), seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da4ce1b8d4e3604b8e546d79003f4d3719223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995106"
---
# <a name="application-directory-partition-security"></a>Seguridad de partición de directorio de aplicaciones

El modelo de control de acceso y seguridad para las particiones de directorio de aplicación es el mismo que el de otras particiones en Active Directory Domain Services. Los usuarios normales pueden tener acceso a los objetos de una partición de directorio de aplicaciones de acuerdo con las ACL colocadas en esos objetos. Para obtener más información, vea [controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Sin embargo, dado que las particiones de directorio de aplicaciones pueden abarcar varios dominios de seguridad en un servicio de directorio, surge la cuestión de cómo interpretar constantes de cadenas de SID conocidas relativas al dominio en el [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la clase de esquema de un objeto en el momento de la creación de un objeto en una partición del directorio de aplicaciones. Por ejemplo, si "DA" hace referencia al grupo administradores de dominio, pero en una partición de directorio de aplicaciones, no se sabe a qué dominio hace referencia el grupo "DA".

Para solucionar este problema, el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) de una partición de directorio de aplicación tiene un atributo [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) que contiene el nombre distintivo del dominio de referencia para esa partición de directorio de aplicaciones. El sistema de seguridad utiliza el dominio especificado para interpretar las referencias de dominio local para los descriptores de seguridad predeterminados adjuntos a los objetos creados en esa partición de directorio de aplicaciones. El dominio de referencia se puede especificar cuando se crea el objeto **crossRef** para una partición de directorio de aplicaciones. Esto requiere, sin embargo, que un objeto **crossRef** se cree previamente para la partición del directorio de aplicaciones. Si no se especifica ningún dominio de referencia, el sistema establece automáticamente el dominio de referencia en función de una de las siguientes condiciones:

-   Si el elemento primario del objeto de partición de directorio de aplicación es otra partición del directorio de aplicaciones, se usa el atributo [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) de la partición del directorio de aplicaciones primaria para el dominio de referencia.
-   Si el objeto primario es un dominio, ese dominio se usa para el dominio de referencia.
-   Si no hay ningún objeto primario, el dominio raíz del bosque se usa para el dominio de referencia.

El atributo **crossRef** también se puede cambiar al dominio de referencia después de crear la partición, pero no se recomienda.

Se produce un problema similar si se especifica un grupo local en una ACL para un objeto en una partición de directorio de aplicaciones. En este caso, el atributo [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) no se puede usar para interpretar el dominio de referencia para un grupo local. Para evitar este problema, no se deben usar grupos locales en las ACL de objetos de partición de directorio de aplicaciones.

 

 