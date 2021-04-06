---
description: El sistema utiliza objetos y controladores para regular el acceso a los recursos del sistema por dos motivos principales.
ms.assetid: 122acb9e-2a1b-480b-9207-5cc6bbe6b6d4
title: Acerca de los identificadores y objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c7474c11298166cc8d63032c6e1d8f84e6db249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002067"
---
# <a name="about-handles-and-objects"></a>Acerca de los identificadores y objetos

El sistema utiliza objetos y controladores para regular el acceso a los recursos del sistema por dos motivos principales. En primer lugar, el uso de objetos garantiza que Microsoft puede actualizar la funcionalidad del sistema, siempre que se mantenga la interfaz de objeto original. Cuando se lancen versiones posteriores del sistema, puede usar el objeto actualizado con pocos o ningún trabajo adicional.

En segundo lugar, el uso de objetos le permite aprovechar la seguridad de Windows. Cada objeto tiene su propia lista de control de acceso (ACL) que especifica las acciones que un proceso puede realizar en el objeto. El sistema examina la ACL de un objeto cada vez que una aplicación crea un identificador para el objeto. Para obtener más información, consulta [Access Control](/windows/desktop/SecAuthZ/access-control).

-   [Administrador de objetos](object-manager.md)
-   [Interfaz de objeto](object-interface.md)
-   [Espacios de nombres de objetos](/windows/desktop/Sync/object-namespaces)
-   [Solucionar limitaciones](handle-limitations.md)
-   [Controlar la herencia](handle-inheritance.md)

 

 
