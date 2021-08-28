---
description: En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM). SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceptos de Administrador de propiedades compartidos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9ce190cb4f4e65e6ab5208dd2adec08f807d4f6d29d4cf99a3e70a1c0a7004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129017"
---
# <a name="com-shared-property-manager-concepts"></a>Conceptos de Administrador de propiedades compartidos de COM+

En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM). SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.

No puede usar variables globales en un entorno distribuido debido a problemas de simultaneidad y colisión de nombres. El administrador de propiedades compartidas elimina las colisiones de nombres al proporcionar grupos de propiedades compartidas, que establecen espacios de nombres únicos para las propiedades compartidas que contienen. SPM también implementa bloqueos y semáforos para ayudar a proteger las propiedades compartidas frente al acceso simultáneo, lo que podría provocar la pérdida de actualizaciones y dejar las propiedades en un estado impredecible.

> [!Note]  
> El estado transitorio compartido es la información de estado que se mantiene en memoria y que no sobrevive a los errores del sistema. La información está diseñada para que la compartan varios objetos entre los límites de transacción (pero no a través del proceso).

 

Las propiedades compartidas almacenadas en SPM solo están disponibles para los objetos que se ejecutan en el mismo proceso. Esto significa que los objetos que usarán SPM para almacenar valores y que deberán tener acceso a estos valores deben instalarse como parte de la misma aplicación COM+. Los administradores del sistema pueden mover clases COM+ de un paquete a otro después de implementar la aplicación COM+. Si se basa en varios objetos que comparten propiedades a través de SPM, debe documentar claramente que deben instalarse en la misma aplicación COM+.

También es importante que los componentes que comparten propiedades tengan el mismo atributo de activación. Si dos componentes del mismo paquete tienen atributos de activación diferentes, por lo general no podrán compartir propiedades. Por ejemplo, si un componente está configurado para ejecutarse en un proceso de cliente y el otro está configurado para ejecutarse en un proceso de servidor, sus objetos normalmente se ejecutarán en procesos diferentes aunque estén en el mismo paquete.

Siempre debe crear instancias de los objetos [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)y [**SharedProperty**](sharedproperty.md) desde componentes COM+ en lugar de desde un cliente base. Si un cliente base crea propiedades y grupos de propiedades compartidos, las propiedades compartidas están dentro del proceso de cliente base, no en un proceso de servidor. Esto significa que los objetos COM+ no pueden compartir las propiedades a menos que los objetos también se ejecuten en el proceso de cliente (lo que generalmente no es una buena idea).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Com+ Shared Administrador de propiedades](com--shared-property-manager.md)
</dt> <dt>

[Grupos de propiedades compartidas](shared-property-groups.md)
</dt> </dl>

 

 



