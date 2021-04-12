---
title: Decidir dónde buscar
description: En este tema se explican las diferentes búsquedas que se pueden realizar en Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidir dónde buscar en AD
- Active Directory AD, buscar, decidir dónde buscar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358794"
---
# <a name="deciding-where-to-search"></a>Decidir dónde buscar

En este tema se explican las diferentes búsquedas que se pueden realizar en Active Directory Domain Services.

Todas las búsquedas se realizan en uno de los siguientes contextos de nomenclatura:

-   Dominio, incluidas las particiones de directorio de aplicaciones
-   Contenedor de esquema
-   Contenedor de configuración
-   Catálogo global

## <a name="searching-a-domain"></a>Buscar un dominio

Los dominios contienen la mayoría de los objetos muy utilizados, como usuarios, contactos, grupos, unidades organizativas, equipos, etc. La mayoría de las consultas buscarán en un dominio. Para obtener más información acerca de la búsqueda de un dominio, vea Buscar en el [contenido del dominio](searching-domain-contents.md).

## <a name="searching-the-schema-container"></a>Buscar en el contenedor de esquemas

El contenedor de esquemas contiene los objetos [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) y [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que proporcionan la definición formal de cada clase y atributo que puede existir en Active Directory Domain Services. Para buscar objetos en el contenedor de esquemas, enlace al contenedor de esquemas en cualquier controlador de dominio. El contenedor de esquema está disponible en todos los controladores de dominio. El nombre distintivo del contenedor de esquema se obtiene del atributo **schemaNamingContext** de RootDSE. Para obtener más información acerca de rootDSE y el atributo **schemaNamingContext** , vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).

Para obtener más información sobre cómo leer el esquema o el contenedor de esquemas abstractos, vea [instrucciones para enlazar con el esquema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Buscar en el contenedor de configuración

El contenedor de configuración contiene información de configuración, como sitios, servicios y especificadores de presentación, para todo el bosque. Para buscar objetos en el contenedor de configuración, enlace al contenedor de configuración en cualquier controlador de dominio. El contenedor de configuración está disponible en todos los controladores de dominio. El nombre distintivo del contenedor de configuración se obtiene del atributo **configurationNamingContext** de RootDSE. Para obtener más información sobre rootDSE y el atributo **configurationNamingContext** , vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).

## <a name="searching-the-global-catalog"></a>Buscar en el catálogo global

El catálogo global contiene una réplica de cada objeto en Active Directory Domain Services, pero solo con un número pequeño de sus atributos. Los atributos del catálogo global son los que se usan con más frecuencia en las operaciones de búsqueda, como el nombre y los apellidos de un usuario, los nombres de inicio de sesión, etc. Para obtener más información acerca de la búsqueda en el catálogo global, vea [Buscar en el catálogo global](searching-global-catalog-contents.md).

 

 