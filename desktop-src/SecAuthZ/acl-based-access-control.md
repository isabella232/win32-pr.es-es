---
description: Al igual que el sistema usa descriptores de seguridad para controlar el acceso a objetos protegibles, un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados. Para obtener más información sobre el Windows de seguridad, vea Access Control Modelo.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Acceso basado en ACL Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073732"
---
# <a name="acl-based-access-control"></a>Acceso basado en ACL Access Control

Al igual que el sistema usa descriptores de seguridad para controlar el acceso a objetos [protegibles,](security-descriptors.md) un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados. Para obtener más información sobre el Windows de seguridad, [vea Access Control Model](access-control-model.md).

Un servidor protegido puede [crear un descriptor de seguridad](security-descriptors-for-private-objects.md) con una DACL que especifica los tipos de acceso permitidos para varios [administradores de confianza.](trustees.md) En un caso simple, el servidor podría crear un descriptor de seguridad único para controlar el acceso a todos los datos y la [funcionalidad del servidor.](checking-access-to-private-objects.md) Para una granularidad más fina de la protección, el servidor podría crear descriptores de seguridad para cada uno de sus objetos privados o para diferentes tipos de funcionalidad.

Por ejemplo, cuando un cliente solicita al servidor que cree un nuevo objeto en una base de datos, el servidor podría crear un descriptor de seguridad para el nuevo objeto privado. A continuación, el servidor podría almacenar el descriptor de seguridad con el objeto privado en la base de datos. Cuando un cliente intenta acceder al objeto , el servidor recupera el descriptor de seguridad para comprobar los derechos de acceso del cliente. Es importante tener en cuenta que no hay nada en un descriptor de seguridad que lo asocie con el objeto o la funcionalidad que protege. En su lugar, es el servidor protegido el que debe mantener la asociación.

También se puede auditar el acceso al objeto privado. Consulte [Auditing Access to Private Objects (Auditoría del](auditing-access-to-private-objects.md) acceso a objetos privados) para obtener una descripción de esto.

 

 



