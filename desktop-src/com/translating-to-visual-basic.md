---
title: Trasladar a Visual Basic
description: Trasladar a Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903602"
---
# <a name="translating-to-visual-basic"></a>Trasladar a Visual Basic

Puede Agregar un objeto COM al proyecto de Visual Basic como una referencia o un componente. Una vez que el objeto se agrega al proyecto, la aplicación puede tener acceso a sus clases e interfaces. A continuación, puede utilizar el Examinador de objetos de Visual Basic para ver la información de la biblioteca de tipos del objeto en Visual Basic sintaxis.

Normalmente, los controles se agregan a un proyecto como componentes y los no Controls se agregan como referencias. Cuando se agrega un objeto COM como componente, aparece en el cuadro de herramientas Visual Basic. Las nuevas instancias de ese objeto se crean arrastrando el icono del objeto desde el cuadro de herramientas hasta un Visual Basic formulario u otro tipo de contenedor. Las nuevas instancias de objetos COM agregados como referencias se crean mediante la palabra clave **New** .

La distinción entre el uso de una clase como referencia frente a un componente es sutil pero importante. Cuando se agrega un objeto como referencia, solo se puede usar la biblioteca de tipos que proporciona el control o la biblioteca de tipos "sin procesar".

Si agrega un control como componente, Visual Basic combina las propiedades y los métodos del extensor del formulario en el que se incrusta el control con la biblioteca de tipos del control, lo que proporciona una versión ajustada y extendida de la biblioteca de tipos. Con esta versión de la biblioteca de tipos, puede usar propiedades de extensor como Top y Left como si formaran parte del control, en lugar del contenedor del control.

En la actualidad, Visual Basic no admite varias bibliotecas de tipos integradas en un único archivo. dll. Si ejecuta en un archivo DLL que incorpora varias bibliotecas de tipos, debe obtener copias independientes de las bibliotecas de tipos del origen que proporcionó el objeto para poder usar el objeto con Visual Basic.

Para obtener más información, vea los temas siguientes:

-   [Trasladar a Visual Basic de C++](translating-to-visual-basic-from-c--.md)
-   [Trasladar a Visual Basic desde Java](translating-to-visual-basic-from-java.md)
-   [Agregar un componente a un proyecto de Visual Basic](adding-a-component-to-a-visual-basic-project.md)
-   [Agregar una referencia a un proyecto de Visual Basic](adding-a-reference-to-a-visual-basic-project.md)
-   [Visual Basic Examinador de objetos](visual-basic-object-browser.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a C++](translating-to-c--.md)
</dt> <dt>

[Traducir a Java](translating-to-java.md)
</dt> </dl>

 

 




