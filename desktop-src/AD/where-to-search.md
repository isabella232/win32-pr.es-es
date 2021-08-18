---
title: Decidir dónde buscar
description: En este tema se explican las distintas búsquedas que se pueden realizar en Active Directory Domain Services.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Decidir dónde buscar AD
- Active Directory AD, buscar, decidir dónde buscar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6984a79bb761c1926b6735a91209c9f387ac45619ffc752daef253a74f5e587a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024323"
---
# <a name="deciding-where-to-search"></a>Decidir dónde buscar

En este tema se explican las distintas búsquedas que se pueden realizar en Active Directory Domain Services.

Todas las búsquedas se realizan en uno de los siguientes contextos de nomenclatura:

-   Dominio, incluidas las particiones de directorio de aplicación
-   Contenedor de esquema
-   Contenedor de configuración
-   Catálogo global

## <a name="searching-a-domain"></a>Búsqueda de un dominio

Los dominios contienen la mayoría de los objetos muy usados, como usuarios, contactos, grupos, unidades organizativas, equipos, entre otros. La mayoría de las consultas buscarán en un dominio. Para obtener más información sobre cómo buscar un dominio, vea [Buscar contenido de dominio.](searching-domain-contents.md)

## <a name="searching-the-schema-container"></a>Buscar en el contenedor de esquemas

El contenedor de esquema contiene los [**objetos classSchema**](/windows/desktop/ADSchema/c-classschema) y [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que proporcionan la definición formal de cada clase y atributo que pueden existir en Active Directory Domain Services. Para buscar objetos en el contenedor de esquemas, enlace al contenedor de esquemas en cualquier controlador de dominio. El contenedor de esquema está disponible en todos los controladores de dominio. El nombre distintivo del contenedor de esquemas se obtiene del atributo **schemaNamingContext** de rootDSE. Para obtener más información sobre rootDSE y el **atributo schemaNamingContext,** vea [Enlace sin servidor y RootDSE.](serverless-binding-and-rootdse.md)

Para obtener más información sobre cómo leer desde el esquema o el contenedor de esquemas abstractos, vea [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).

## <a name="searching-the-configuration-container"></a>Buscar en el contenedor de configuración

El contenedor de configuración contiene información de configuración, como sitios, servicios y especificadores de pantalla, para todo el bosque. Para buscar objetos en el contenedor de configuración, enlace al contenedor de configuración en cualquier controlador de dominio. El contenedor de configuración está disponible en todos los controladores de dominio. El nombre distintivo del contenedor de configuración se obtiene del **atributo configurationNamingContext** de rootDSE. Para obtener más información sobre rootDSE y el **atributo configurationNamingContext,** vea [Enlace sin servidor y RootDSE.](serverless-binding-and-rootdse.md)

## <a name="searching-the-global-catalog"></a>Búsqueda en el catálogo global

El catálogo global contiene una réplica de todos los objetos Active Directory Domain Services, pero con solo un pequeño número de sus atributos. Los atributos del catálogo global son los que se usan con más frecuencia en las operaciones de búsqueda, como los nombres y apellidos de un usuario, los nombres de inicio de sesión, y así sucesivamente. Para obtener más información sobre cómo buscar en el catálogo global, vea [Buscar en el catálogo global.](searching-global-catalog-contents.md)

 

 