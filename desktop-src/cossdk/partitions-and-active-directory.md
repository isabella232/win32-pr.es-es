---
description: Además de las particiones, que contienen una o más aplicaciones, COM+ también incluye conjuntos de particiones, que contienen una o más particiones.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Particiones y Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677217"
---
# <a name="partitions-and-active-directory"></a>Particiones y Active Directory

Además de las particiones, que contienen una o más aplicaciones, COM+ también incluye *conjuntos de particiones*, que contienen una o más particiones. Creado en Active Directory, los conjuntos de particiones permiten a los usuarios de un dominio obtener acceso a las aplicaciones COM+ en todo el dominio. Durante la creación, cada usuario o unidad organizativa (OU) específico se asigna, o se asigna, a un conjunto de particiones.

Un solo usuario o unidad organizativa puede tener acceso a varias particiones y sus aplicaciones, ya que hay una correlación uno a uno entre una identidad de usuario o una unidad organizativa y un conjunto de particiones. Sin un conjunto de particiones, un usuario o una unidad organizativa necesitaría varias identidades de usuario para obtener acceso a las aplicaciones en diferentes particiones.

Para que las aplicaciones COM+ estén disponibles para los usuarios del dominio, un administrador debe realizar tareas en el controlador de dominio en el que reside Active Directory y en el servidor en el que está instalada la aplicación COM+.

## <a name="on-the-domain-controller"></a>En el controlador de dominio

En primer lugar, el administrador crea una partición dentro de Active Directory. La creación de una partición COM+ se realiza mediante el uso de la Active Directory herramienta administrativa usuarios y equipos o mediante programación con la interfaz de Active Directory Services (ADSI).

Una vez creada la partición en Active Directory, el administrador crea un conjunto de particiones. Al crear un conjunto de particiones, el administrador define las particiones que se incluyen en ese conjunto. La creación de un conjunto de particiones COM+ se realiza mediante el uso de la Active Directory herramienta administrativa usuarios y equipos o mediante programación con la interfaz de Active Directory Services (ADSI).

Por último, el administrador asigna usuarios de dominio o unidades organizativas (OU) al conjunto de particiones recién creado. Para ello, se muestra la página de **propiedades** de un usuario, el acceso a la pestaña **conjuntos de particiones com+** y la selección de un conjunto de particiones en el cuadro de lista.

## <a name="on-the-com-application-server"></a>En el servidor de aplicaciones COM+

El administrador crea una nueva partición, especificando el mismo nombre de partición y el mismo identificador de partición (GUID) que el de la partición que se creó en Active Directory en el controlador de dominio. Esto se hace mediante la carpeta **particiones com+** dentro de la herramienta administrativa Servicios de componentes. Para simplificar esta tarea, la herramienta servicios de componentes permite al administrador examinar Active Directory para seleccionar la partición deseada y su GUID.

Cuando se ha creado la partición de dominio en el servidor de aplicaciones, la partición predeterminada de un usuario se convierte en la partición predeterminada del conjunto de particiones en el Active Directory. Por último, el administrador puede instalar la aplicación COM+ en la partición recién creada en el servidor de aplicaciones.

Para obtener más información acerca de la administración de particiones para el acceso de usuarios de dominio, consulte la ayuda asociada a la herramienta administrativa usuarios y equipos de Active Directory.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Asignación de identidades de usuario y unidades organizativas a conjuntos de particiones

Los usuarios y las unidades organizativas se pueden asignar a un conjunto de particiones. Al asignar unidades organizativas a conjuntos de particiones, un administrador puede asociar varios usuarios a un conjunto de particiones al mismo tiempo en lugar de tener que asignar varias identidades de usuario. Una sola identidad de usuario o unidad organizativa solo se puede asignar a un conjunto de particiones. En general, la asignación de identidades de usuario o unidades organizativas a conjuntos de particiones hace lo siguiente:

-   Garantiza que las aplicaciones estén disponibles para los usuarios adecuados en el dominio.
-   Ayuda a COM+ a determinar la partición en la que se encuentra una aplicación
-   Establece el derecho de un usuario para tener acceso a una aplicación determinada.

Para asociar particiones con conjuntos de particiones dentro de Active Directory y asignar usuarios y unidades organizativas a esos conjuntos de particiones, los administradores usan las herramientas administrativas usuarios y equipos y servicios de componentes de Active Directory. Cuando se crea una partición en Active Directory, un administrador debe configurar localmente esa partición en el equipo en el que se va a instalar la aplicación COM+ pertinente. Esta configuración local de las particiones creadas en Active Directory se realiza a través de la herramienta administrativa Servicios de componentes.

Si una identidad de usuario de dominio no está asignada a un conjunto de particiones, el usuario recibe el acceso a la unidad organizativa del usuario, que se asigna a la partición. Si la unidad organizativa del usuario no está asignada a un conjunto de particiones, pero la siguiente unidad organizativa más alta de la jerarquía está asignada a ese conjunto de particiones, el usuario puede tener acceso a la partición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones predeterminadas](default-partitions.md)
</dt> <dt>

[Particiones locales](local-partitions.md)
</dt> <dt>

[Propiedades de la partición](partition-properties.md)
</dt> <dt>

[La partición global](the-global-partition.md)
</dt> </dl>

 

 



