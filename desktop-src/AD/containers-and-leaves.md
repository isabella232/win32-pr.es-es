---
title: Contenedores y hojas
description: Active Directory Domain Services contienen una jerarquía de objetos en la que todas las instancias de objeto, excepto la raíz de la jerarquía de directorios, están contenidas en otro objeto.
ms.assetid: ef17e84c-6c7f-4ebe-a904-fead6c27518d
ms.tgt_platform: multiple
keywords:
- contenedores y hojas Active Directory
- Active Directory hoja
- Active Directory de contenedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9039e4619ea0bd50d20c3bd425b6a8536a1034
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487486"
---
# <a name="containers-and-leaves"></a>Contenedores y hojas

Active Directory Domain Services contienen una jerarquía de objetos en la que todas las instancias de objeto, excepto la raíz de la jerarquía de directorios, están contenidas en otro objeto. La estructura de esta jerarquía es más flexible que un sistema de archivos de directorios y archivos. En su lugar, las reglas, en el [esquema de Active Directory](active-directory-schema.md), determinan qué clases de objeto pueden contener instancias de otras clases de objeto. Por ejemplo, la definición de esquema predeterminada de la clase de objeto de [**usuario**](/windows/desktop/ADSchema/c-user) incluye las clases de [**unidad organizativa**](/windows/desktop/ADSchema/c-organizationalunit) y de objeto [**contenedor**](/windows/desktop/ADSchema/c-container) como posibles superiores; es decir, posibles objetos primarios o contenedores de una instancia de objeto de **usuario** . Esto significa que un objeto **de unidad organizativa** puede contener un objeto de **usuario** , pero un objeto de **usuario** no puede contener otro objeto de **usuario** , a menos que se cambie la definición de esquema de la clase de **usuario** .

Excepto en el caso de los objetos de esquema, es decir, los objetos [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) o [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) que definen las clases y los atributos que pueden existir en un bosque de servidor, cualquier objeto de Active Directory Domain Services puede ser un contenedor. En concreto, cualquier clase de objeto que aparezca en el atributo [**possSuperiors**](/windows/desktop/ADSchema/a-posssuperiors) o [**systemPossSuperiors**](/windows/desktop/ADSchema/a-systemposssuperiors) de una definición de clase de objeto es potencialmente un contenedor. Para obtener más información sobre los contenedores de una clase de objeto predefinida, vea [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md). Puede enlazar mediante programación al esquema abstracto y usar los métodos [**IADsClass:: get \_ contain**](/windows/desktop/api/iads/nn-iads-iadsclass) o [**IADsClass:: get \_ PossibleSuperiors**](/windows/desktop/api/iads/nn-iads-iadsclass) para obtener las clases que una clase determinada puede contener o incluir. Para obtener más información, vea [leer el esquema abstracto](reading-the-abstract-schema.md). También puede leer el atributo [**possibleInferiors**](/windows/desktop/ADSchema/a-possibleinferiors) de cualquier instancia de objeto para determinar las clases de objeto que puede contener el objeto. Tenga en cuenta que **possibleInferiors** es un atributo construido, lo que significa que se calcula a partir de los valores de **possSuperiors** / **systemPossSuperiors** de las demás definiciones de clase y que realmente no se almacena en el directorio.

Tenga en cuenta que el esquema de Active Directory define una clase [**contenedora**](/windows/desktop/ADSchema/c-container) . Como se explicó anteriormente, no es necesario que un objeto sea una instancia de la clase **contenedora** como contenedor. También hay una clase [**hoja**](/windows/desktop/ADSchema/c-leaf) y, aunque las subclases de esta clase no suelen ser contenedores, no hay ningún motivo por el que no sea posible.

Por último, puede establecer una marca en el especificador de presentación asociado a una clase de objeto para indicar que las interfaces de usuario deben mostrar siempre las instancias de la clase como hojas en lugar de contenedores. Esto ayuda a evitar que la interfaz de usuario esté abarrotada en demasiados contenedores. Para obtener más información, vea [Ver contenedores como nodos de hoja](viewing-containers-as-leaf-nodes.md).

 

 