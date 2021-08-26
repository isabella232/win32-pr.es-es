---
title: Agregar una referencia a un Visual Basic Project
description: Agregar una referencia a un Visual Basic Project
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deba6030e57839e0f436239790aaa6f02e2fb29981ce021b0de2d09af2acdff6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097075"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a>Agregar una referencia a un Visual Basic Project

En el procedimiento siguiente se describe cómo agregar una referencia a un objeto COM a un Visual Basic proyecto. A continuación, la aplicación puede usar las clases de ese objeto.

Al agregar un objeto como referencia, solo puede usar la biblioteca de tipos proporcionada por el control o la biblioteca de tipos "sin procesar". Por el contrario, agregar un control como componente también expone las propiedades Visual Basic y los métodos extensores como si formasen parte del control.

**Para hacer una Visual Basic referencia a un componente**

1.  En el menú **Proyecto**, haga clic en **Referencias**.
2.  Haga clic para activar la casilla situada junto al componente que desea agregar. Si el componente no aparece, busque el archivo .dll o .ocx mediante **Examinar**.
3.  Haga clic en **Aceptar**.

El componente ahora forma parte del proyecto. La aplicación puede crear instancias de clase mediante la **palabra clave New.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregar un componente a un Visual Basic Project](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[Traducción a Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 




