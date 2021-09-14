---
description: Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan distintos niveles de organización de la directiva de Authorization Manager.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Almacenes de directivas, aplicaciones y ámbitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265463"
---
# <a name="policy-stores-applications-and-scopes"></a>Almacenes de directivas, aplicaciones y ámbitos

Los almacenes de directivas de autorización, las aplicaciones y los ámbitos representan distintos niveles de organización de la directiva de Authorization Manager. Un almacén de directivas puede contener una o varias aplicaciones y una aplicación puede contener uno o varios ámbitos.

-   [Almacenes de directivas de autorización](#authorization-policy-stores)
-   [Aplicaciones](#policy-stores-applications-and-scopes)
-   [Ámbitos](#policy-stores-applications-and-scopes)
-   [Delegación](#delegation)
-   [Temas relacionados](#related-topics)

## <a name="authorization-policy-stores"></a>Almacenes de directivas de autorización

En la API del Administrador de autorización, un almacén de directivas de autorización se representa mediante un [**objeto IAzAuthorizationStore.**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) El almacén de directivas de autorización contiene definiciones y asignaciones de aplicaciones, ámbitos, operaciones, tareas, roles y grupos de usuarios.

Un almacén de directivas de autorización se puede almacenar como un archivo XML o en Active Directory.

Una aplicación debe inicializar un almacén de directivas de autorización antes de cambiar la información del almacén o usar la directiva de almacén para comprobar el acceso del cliente a los recursos.

Un almacén de directivas de autorización puede contener uno o varios [**objetos IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) que representan la directiva de autorización para una aplicación específica.

## <a name="applications"></a>Aplicaciones

En la API del Administrador de autorización, una aplicación se representa mediante un [**objeto IAzApplication.**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) Un almacén de directivas de autorización puede contener información de directiva de autorización para muchas aplicaciones. El **uso de objetos IAzApplication** permite almacenar una directiva de autorización diferente para distintas aplicaciones en un único almacén de directivas.

Un almacén de directivas de autorización debe contener al menos una aplicación.

## <a name="scopes"></a>Ámbitos

En la API del Administrador de autorización, un ámbito se representa mediante un [**objeto IAzScope.**](/windows/desktop/api/Azroles/nn-azroles-iazscope) Los ámbitos proporcionan un nivel adicional opcional de organización para una directiva de autorización. Una aplicación puede contener uno o varios ámbitos, pero no debe contener ninguno (el Administrador de autorización proporciona un ámbito predeterminado para toda la aplicación).

Un ámbito es una subdivisión dentro de una aplicación que separa los recursos de otros recursos que usa esa aplicación. Si existen grupos, asignaciones de funciones, definiciones de función o definiciones de tarea de Administrador de autorización que no desea implementar en toda una aplicación, puede crearlos en el nivel del ámbito.

## <a name="delegation"></a>Delegación

Los almacenes de directivas de autorización que se almacenan en Active Directory admiten la delegación de administración. La administración se puede delegar a usuarios y grupos en el nivel de almacén, aplicación o ámbito. Cada nivel define roles administrativos para la directiva en ese nivel. Para delegar el control en un usuario o grupo, asígnelos al rol de administrador; para permitir que un usuario o grupo lea la directiva, asígnelos al rol de lector.

Los administradores de un almacén, aplicación o ámbito pueden leer y modificar el almacén de directivas en el nivel delegado. Los lectores pueden leer el almacén de directivas en el nivel delegado, pero no pueden modificar el almacén.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[Creación de un objeto de aplicación en C++](creating-an-application-object-in-c--.md)
</dt> <dt>

[Delegación de la definición de permisos en C++](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



