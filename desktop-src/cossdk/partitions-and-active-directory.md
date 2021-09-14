---
description: Además de las particiones, que contienen una o varias aplicaciones, COM+ también incluye conjuntos de particiones, que contienen una o varias particiones.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Particiones y Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888937"
---
# <a name="partitions-and-active-directory"></a>Particiones y Active Directory

Además de las particiones, que contienen una o varias aplicaciones, COM+ también incluye conjuntos de particiones *,* que contienen una o varias particiones. Creados en Active Directory, los conjuntos de particiones permiten a los usuarios de un dominio acceder a aplicaciones COM+ en todo el dominio. Durante la creación, cada usuario o unidad organizativa (OU) específico se asigna o asigna a un conjunto de particiones.

Un único usuario o unidad organizativa puede acceder a varias particiones y sus aplicaciones porque hay una correlación uno a uno entre una identidad de usuario o unidad organizativa y un conjunto de particiones. Sin un conjunto de particiones, un usuario u unidad organizativa necesitará varias identidades de usuario para acceder a las aplicaciones de diferentes particiones.

Para que las aplicaciones COM+ estén disponibles para los usuarios del dominio, un administrador debe realizar tareas tanto en el controlador de dominio donde reside Active Directory como en el servidor donde está instalada la aplicación COM+.

## <a name="on-the-domain-controller"></a>En el controlador de dominio

En primer lugar, el administrador crea una partición Active Directory. La creación de una partición COM+ se realiza mediante el uso de la herramienta administrativa Usuarios y equipos de Active Directory o mediante programación mediante la interfaz de Active Directory Services (ADSI).

Una vez creada la partición en Active Directory, el administrador crea un conjunto de particiones. Al crear un conjunto de particiones, el administrador define las particiones que se incluyen en ese conjunto. La creación de un conjunto de particiones COM+ se realiza mediante el uso de la herramienta administrativa Usuarios y equipos de Active Directory o mediante programación mediante la interfaz de Active Directory Services (ADSI).

Por último, el administrador asigna usuarios de dominio o unidades organizativas (unidades organizativas) al conjunto de particiones recién creado. Para ello, se muestra  la página Propiedades de un usuario, se accede a la pestaña Conjuntos de particiones **com+** y se selecciona un conjunto de particiones en el cuadro de lista.

## <a name="on-the-com-application-server"></a>En el servidor de aplicaciones COM+

El administrador crea una nueva partición, especificando el mismo nombre de partición y el mismo identificador de partición (GUID) que el de la partición que se creó Active Directory en el controlador de dominio. Esto se hace mediante la **carpeta Particiones COM+** dentro de la herramienta administrativa Servicios de componentes. Para simplificar esta tarea, la herramienta Servicios de componentes permite al administrador examinar Active Directory seleccionar la partición deseada y su GUID.

Cuando se ha creado la partición de dominio en el servidor de aplicaciones, la partición predeterminada de un usuario se convierte en la partición predeterminada del conjunto de particiones en el Active Directory. Por último, el administrador puede instalar la aplicación COM+ en la partición recién creada en el servidor de aplicaciones.

Para obtener más información sobre cómo administrar particiones para el acceso por parte de los usuarios del dominio, consulte la ayuda asociada con la Usuarios y equipos de Active Directory administrativa.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Asignación de identidades de usuario y us a conjuntos de particiones

Los usuarios y las unidades de unidades de disco se pueden asignar a conjuntos de particiones. Al asignar us a conjuntos de particiones, un administrador puede asociar varios usuarios a un conjunto de particiones a la vez en lugar de tener que asignar varias identidades de usuario. Una única identidad de usuario o unidad organizativa solo se puede asignar a un conjunto de particiones. En general, la asignación de identidades de usuario o us a conjuntos de particiones hace lo siguiente:

-   Garantiza que las aplicaciones están disponibles para los usuarios adecuados en el dominio.
-   Ayuda a COM+ a determinar la partición en la que se encuentra una aplicación
-   Establece el derecho de un usuario a acceder a una aplicación determinada.

Para asociar particiones con conjuntos de particiones dentro de Active Directory y para asignar usuarios y utiles a esos conjuntos de particiones, los administradores usan las herramientas administrativas Usuarios y equipos de Active Directory y Servicios de componentes. Cuando se crea una partición en Active Directory, un administrador debe configurar localmente esa partición en el equipo donde se va a instalar la aplicación COM+ correspondiente. Esta configuración local de particiones creadas en Active Directory se realiza a través de la herramienta administrativa Servicios de componentes.

Si una identidad de usuario de dominio no está asignada a un conjunto de particiones, la unidad organizativa del usuario concede al usuario acceso, que se asigna a la partición. Si la unidad organizativa del usuario no está asignada a un conjunto de particiones, pero la siguiente unidad organizativa más alta de la jerarquía está asignada a ese conjunto de particiones, el usuario puede acceder a la partición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Particiones predeterminadas](default-partitions.md)
</dt> <dt>

[Particiones locales](local-partitions.md)
</dt> <dt>

[Propiedades de partición](partition-properties.md)
</dt> <dt>

[La partición global](the-global-partition.md)
</dt> </dl>

 

 



