---
title: Herencia de clases en el esquema de Active Directory
description: Todas las clases de objeto de un esquema del servicio de directorio de Active Directory se derivan de la clase especial Top.
ms.assetid: 26e5107f-8204-4f64-bd07-b5b4f16103f4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd550a3eed6aeb633f6db265260b6c65c17f993
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077558"
---
# <a name="class-inheritance-in-the-active-directory-schema"></a>Herencia de clases en el esquema de Active Directory

Todas las clases de objeto de un esquema del servicio de directorio de Active Directory se derivan de la clase especial [**Top**](/windows/desktop/ADSchema/c-top). Con la excepción de **Top**, todas las clases de objeto son subclases de otra clase de objeto. Por ejemplo, [**Contact**](/windows/desktop/ADSchema/c-contact) es una subclase de [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson); **OrganizationalPerson** es una subclase de [**Person**](/windows/desktop/ADSchema/c-person); y **Person** es una subclase de **Top**. El atributo [**Subclassa**](/windows/desktop/ADSchema/a-subclassof) de un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) es una propiedad de un solo valor que indica la superclase inmediata de la clase.

Algunos de los valores de atributo que definen una clase se heredan de sus superclases. Por lo tanto, la clase [**Contact**](/windows/desktop/ADSchema/c-contact) hereda valores de sus superclases, que son las clases [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson), [**Person**](/windows/desktop/ADSchema/c-person)y [**Top**](/windows/desktop/ADSchema/c-top) . Una clase hereda los siguientes datos de sus superclases:

-   Posibles atributos: los valores de los atributos [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)y [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) de un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) definen una lista completa de los atributos que se pueden establecer en una instancia de la clase de objeto. Para cada clase de objeto, los valores de estos atributos incluyen todos los valores que se heredan de sus superclases, así como los valores que se establecen explícitamente para la propia clase de objeto. Por lo tanto, el atributo [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) de la clase [**OrganizationalPerson**](/windows/desktop/ADSchema/c-organizationalperson) incluye todos los valores de **mustContain** que se heredan de las clases [**Person**](/windows/desktop/ADSchema/c-person) y [**Top**](/windows/desktop/ADSchema/c-top) , así como los valores **mustContain** que se establecen explícitamente en la clase **OrganizationalPerson** .
-   Posibles elementos primarios en la jerarquía de directorios: los valores de los atributos [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) y [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) de un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) definen una lista completa de las clases de objeto que pueden contener una instancia de la clase de objeto. Para cada clase de objeto, los valores incluyen los heredados de sus superclases, así como los que se establecen explícitamente para la propia clase de objeto.

Tenga en cuenta que la clase de objeto también puede tener muchas clases auxiliares, que se especifican en los atributos [**auxiliaryClass**](/windows/desktop/ADSchema/a-auxiliaryclass) y [**systemAuxiliaryClass**](/windows/desktop/ADSchema/a-systemauxiliaryclass) de un objeto **ClassSchema** . Una clase de objeto hereda los valores [**mustContain**](/windows/desktop/ADSchema/a-mustcontain), [**mayContain**](/windows/desktop/ADSchema/a-maycontain), [**systemMustContain**](/windows/desktop/ADSchema/a-systemmustcontain)y [**systemMayContain**](/windows/desktop/ADSchema/a-systemmaycontain) de sus clases auxiliares.

 

 