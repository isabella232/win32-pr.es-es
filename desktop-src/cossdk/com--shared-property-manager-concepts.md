---
description: En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM). SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceptos de Administrador de propiedades compartidos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714873"
---
# <a name="com-shared-property-manager-concepts"></a>Conceptos de Administrador de propiedades compartidos de COM+

En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM). SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.

Las variables globales no se pueden usar en un entorno distribuido debido a problemas de simultaneidad y conflicto de nombres. El administrador de propiedades compartidas elimina los conflictos de nombres al proporcionar grupos de propiedades compartidas, que establecen espacios de nombres únicos para las propiedades compartidas que contienen. SPM también implementa bloqueos y semáforos para ayudar a proteger las propiedades compartidas de acceso simultáneo, lo que podría provocar la pérdida de actualizaciones y dejar propiedades en un estado impredecible.

> [!Note]  
> El estado transitorio compartido es la información de estado conservada en memoria que no sobrevive los errores del sistema. La información está diseñada para que la compartan varios objetos a través de los límites de transacciones (pero no entre procesos).

 

Las propiedades compartidas almacenadas en SPM solo están disponibles para los objetos que se ejecutan en el mismo proceso. Esto significa que los objetos que utilizarán SPM para almacenar valores y que necesitarán tener acceso a estos valores se deben instalar como parte de la misma aplicación COM+. Los administradores del sistema pueden trasladar las clases COM+ de un paquete a otro una vez implementada la aplicación COM+. Si confía en varios objetos que comparten propiedades a través de SPM, debe documentar claramente que deben instalarse en la misma aplicación COM+.

También es importante que los componentes que comparten propiedades tengan el mismo atributo de activación. Si dos componentes del mismo paquete tienen atributos de activación diferentes, por lo general no podrán compartir propiedades. Por ejemplo, si un componente está configurado para ejecutarse en un proceso de cliente y el otro está configurado para ejecutarse en un proceso de servidor, sus objetos normalmente se ejecutarán en procesos diferentes, aunque estén en el mismo paquete.

Siempre debe crear una instancia de los objetos [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)y [**SharedProperty**](sharedproperty.md) a partir de los componentes com+ en lugar de hacerlo desde un cliente base. Si un cliente base crea propiedades y grupos de propiedades compartidas, las propiedades compartidas se encuentran dentro del proceso de cliente base, no en un proceso de servidor. Esto significa que los objetos COM+ no pueden compartir las propiedades a menos que los objetos también se ejecuten en el proceso del cliente (que no suele ser una buena idea).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de propiedades compartidos de COM+](com--shared-property-manager.md)
</dt> <dt>

[Grupos de propiedades compartidas](shared-property-groups.md)
</dt> </dl>

 

 



