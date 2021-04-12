---
title: Agregar una referencia a un proyecto de Visual Basic
description: Agregar una referencia a un proyecto de Visual Basic
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356949"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Agregar una referencia a un proyecto de Visual Basic

En el procedimiento siguiente se describe cómo agregar una referencia a un objeto COM en un proyecto Visual Basic. A continuación, la aplicación puede usar las clases de ese objeto.

Cuando se agrega un objeto como referencia, solo se puede utilizar la biblioteca de tipos proporcionada por el control o la biblioteca de tipos "sin procesar". En cambio, al agregar un control como componente también se exponen las propiedades y los métodos del extensor Visual Basic como si formaran parte del control.

**Para hacer referencia Visual Basic a un componente**

1.  En el menú **Proyecto**, haga clic en **Referencias**.
2.  Active la casilla situada junto al componente que desee agregar. Si el componente no aparece en la lista, busque el archivo. dll o. ocx mediante **examinar**.
3.  Haga clic en **OK**.

El componente ahora forma parte del proyecto. La aplicación puede crear instancias de clase mediante la palabra clave **New** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar un componente a un proyecto de Visual Basic](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Trasladar a Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




