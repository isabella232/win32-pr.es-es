---
title: Controlar el acceso a los objetos y sus propiedades
description: Para controlar el acceso a los objetos de la aplicación, trabaje con el descriptor de seguridad del objeto y, en concreto, con la lista de control de acceso discrecional (DACL) y su lista de entradas de control de acceso (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- objeto AD, controlar el acceso a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268229"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>Controlar el acceso a los objetos y sus propiedades

Para controlar el acceso a los objetos de la aplicación, trabaje con el descriptor de seguridad del objeto y, en concreto, con la lista de control de acceso discrecional (DACL) y su lista de entradas de control de acceso (ACE).

Cuando se crea un objeto, recibe un descriptor de seguridad. Para obtener más información y una descripción de las reglas que utiliza el sistema para crear la DACL para un nuevo objeto, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](how-security-descriptors-are-set-on-new-directory-objects.md). Estas reglas muestran que puede:

-   Cree un nuevo descriptor de seguridad y asócielo al objeto en el momento de su creación. Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto de directorio](creating-a-security-descriptor-for-a-new-directory-object.md).
-   Aplique una ACE heredable, en cualquier punto de la jerarquía de directorios, de modo que los objetos de una ACE hereden el árbol. Un objeto puede heredar una ACE de su contenedor primario. Para obtener más información, vea [herencia y delegación de la administración](inheritance-and-delegation-of-administration.md).
-   Especifique una ACE en la DACL predeterminada en el esquema, si tiene los derechos de acceso necesarios. Cada definición de clase de objeto del esquema incluye un descriptor de seguridad predeterminado que puede tener una DACL predeterminada. Para obtener más información, vea [descriptor de seguridad predeterminado](default-security-descriptor.md).

Además, se puede modificar la DACL de un objeto existente. Puede:

-   Reemplace la DACL por otra nueva.
-   Leer la DACL existente, modificarla y aplicar la DACL modificada. Para obtener más información, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

En la lista siguiente se describe la función más importante de una ACE en Active Directory Domain Services. Con una ACE, puede:

-   Controlar quién puede realizar operaciones concretas en un objeto.
-   Controla quién tiene acceso a una propiedad concreta o a un conjunto de propiedades de un objeto.
-   Controlar quién puede crear objetos secundarios en un contenedor, incluido quién puede crear un tipo específico de objeto secundario.
-   Definir derechos de acceso de control privado para un tipo de objeto y controlar quién puede realizar las operaciones protegidas por los derechos privados.
-   Aplique una ACE a un objeto contenedor en la raíz de un subárbol de directorio, de modo que todos los objetos secundarios del árbol puedan heredar automáticamente las protecciones.
-   Aplicar una ACE heredada automáticamente por un tipo específico de objeto secundario en un subárbol.
-   Cree una ACE que conceda derechos a un grupo de seguridad, en lugar de a un solo usuario.
-   Aplique una ACE a directiva de grupo objetos para controlar las cuentas y los equipos afectados por la Directiva.

 

 




