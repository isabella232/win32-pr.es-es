---
description: Del mismo modo que el sistema usa descriptores de seguridad para controlar el acceso a los objetos protegibles, un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados. Para obtener más información sobre el modelo de seguridad de Windows, vea modelo de Access Control.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Access Control basados en ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813286"
---
# <a name="acl-based-access-control"></a>Access Control basados en ACL

Del mismo modo que el sistema usa [descriptores de seguridad](security-descriptors.md) para controlar el acceso a los objetos protegibles, un servidor puede usar descriptores de seguridad para controlar el acceso a sus objetos privados. Para obtener más información sobre el modelo de seguridad de Windows, vea [modelo de Access Control](access-control-model.md).

Un servidor protegido puede [crear un descriptor de seguridad](security-descriptors-for-private-objects.md) con una DACL que especifique los tipos de acceso permitidos para varios [confíantes](trustees.md). En un caso sencillo, el servidor podría crear un único descriptor [de seguridad para controlar el acceso a todos los datos y la funcionalidad del servidor](checking-access-to-private-objects.md). Para una granularidad más fina de protección, el servidor podría crear descriptores de seguridad para cada uno de sus objetos privados o para diferentes tipos de funcionalidad.

Por ejemplo, cuando un cliente solicita al servidor que cree un nuevo objeto en una base de datos, el servidor podría crear un descriptor de seguridad para el nuevo objeto privado. Después, el servidor podría almacenar el descriptor de seguridad con el objeto privado en la base de datos. Cuando un cliente intenta obtener acceso al objeto, el servidor recupera el descriptor de seguridad para comprobar los derechos de acceso del cliente. Es importante tener en cuenta que no hay nada en un descriptor de seguridad que lo asocie con el objeto o la funcionalidad que protege. En su lugar, es el servidor protegido el que mantiene la asociación.

También se puede auditar el acceso al objeto privado. Consulte [Auditoría de acceso a objetos privados](auditing-access-to-private-objects.md) para obtener una descripción de este.

 

 



