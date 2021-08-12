---
title: Traducción a Visual Basic
description: Traducción a Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9aa8a163141c6361df464a22ce873770c8385607bdf8f84d333d204c55a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550619"
---
# <a name="translating-to-visual-basic"></a>Traducción a Visual Basic

Puede agregar un objeto COM al proyecto Visual Basic como referencia o como componente. Una vez que el objeto se agrega al proyecto, la aplicación puede acceder a sus clases e interfaces. A continuación, puede usar Visual Basic Explorador de objetos para ver la información de la biblioteca de tipos del objeto en Visual Basic sintaxis.

Normalmente, los controles se agregan a un proyecto como componentes y noncontrols se agregan como referencias. Cuando se agrega un objeto COM como componente, aparece en el cuadro Visual Basic de herramientas. Las nuevas instancias de ese objeto se crean arrastrando el icono de objeto desde el cuadro de herramientas a Visual Basic formulario u otro tipo de contenedor. Las nuevas instancias de objetos COM agregados como referencias se crean mediante la **palabra clave new.**

La distinción entre usar una clase como referencia frente a un componente es sutil pero importante. Al agregar un objeto como referencia, solo puede usar la biblioteca de tipos que proporciona el control o la biblioteca de tipos "sin formato".

Si agrega un control como componente, Visual Basic combina las propiedades extensores y los métodos del formulario en el que el control se incrusta con la biblioteca de tipos del control, lo que proporciona una versión ajustada y extendida de la biblioteca de tipos. Con esta versión de la biblioteca de tipos, puede usar propiedades extensores como Top e Left como si formas parte del control, en lugar del contenedor del control.

Visual Basic admite actualmente varias bibliotecas de tipos integradas en un único .dll archivo. Si se encuentra con un archivo DLL que incorpora varias bibliotecas de tipos, debe obtener copias independientes de las bibliotecas de tipos del origen que proporcionó el objeto para usar el objeto con Visual Basic.

Para obtener más información, vea los temas siguientes:

-   [Traducción a Visual Basic desde C++](translating-to-visual-basic-from-c--.md)
-   [Traducción a Visual Basic desde Java](translating-to-visual-basic-from-java.md)
-   [Agregar un componente a un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
-   [Agregar una referencia a un Visual Basic Project](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Explorador de objetos](visual-basic-object-browser.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> <dt>

[Traducción a Java](translating-to-java.md)
</dt> </dl>

 

 




