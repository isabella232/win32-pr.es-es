---
description: Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan diferentes niveles de organización de la Directiva de administrador de autorización.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Almacenes de directivas, aplicaciones y ámbitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908179"
---
# <a name="policy-stores-applications-and-scopes"></a>Almacenes de directivas, aplicaciones y ámbitos

Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan diferentes niveles de organización de la Directiva de administrador de autorización. Un almacén de directivas puede contener una o más aplicaciones, y una aplicación puede contener uno o más ámbitos.

-   [Almacenes de directivas de autorización](#authorization-policy-stores)
-   [Aplicaciones](#policy-stores-applications-and-scopes)
-   [Ámbitos](#policy-stores-applications-and-scopes)
-   [Delegación](#delegation)
-   [Temas relacionados](#related-topics)

## <a name="authorization-policy-stores"></a>Almacenes de directivas de autorización

En la API de administrador de autorización, un almacén de directivas de autorización se representa mediante un objeto [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) . El almacén de directivas de autorización contiene definiciones y asignaciones de aplicaciones, ámbitos, operaciones, tareas, roles y grupos de usuarios.

Un almacén de directivas de autorización puede almacenarse como un archivo XML o en Active Directory.

Una aplicación debe inicializar un almacén de directivas de autorización antes de cambiar la información del almacén o de usar la Directiva de la tienda para comprobar el acceso del cliente a los recursos.

Un almacén de directivas de autorización puede contener uno o más objetos [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) , cada uno de los cuales representa una directiva de autorización para una aplicación específica.

## <a name="applications"></a>APLICACIONES

En la API de administrador de autorización, una aplicación se representa mediante un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) . Un almacén de directivas de autorización puede contener información de directiva de autorización para muchas aplicaciones. El uso de objetos **IAzApplication** permite almacenar diferentes directivas de autorización para diferentes aplicaciones en un único almacén de directivas.

Un almacén de directivas de autorización debe contener al menos una aplicación.

## <a name="scopes"></a>Ámbitos

En la API de administrador de autorización, un ámbito se representa mediante un objeto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) . Los ámbitos proporcionan un nivel de organización adicional y opcional para una directiva de autorización. Una aplicación puede contener uno o más ámbitos, pero no es necesario que tenga (el administrador de autorización proporciona un ámbito predeterminado de toda la aplicación).

Un ámbito es una subdivisión dentro de una aplicación que separa los recursos de otros recursos utilizados por esa aplicación. Si existen grupos, asignaciones de funciones, definiciones de función o definiciones de tarea de Administrador de autorización que no desea implementar en toda una aplicación, puede crearlos en el nivel del ámbito.

## <a name="delegation"></a>Delegación

Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de la administración. La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito. Cada nivel define roles administrativos para la Directiva en ese nivel. Para delegar el control a un usuario o grupo, asígnelos al rol de administrador; para permitir que un usuario o grupo Lea la Directiva, asígnela al rol lector.

Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado. Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Crear un objeto de aplicación en C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delegación de la definición de permisos en C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



