---
title: Elemento ShapeType de VML
description: Elemento ShapeType de VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0632919a141ae04f80b0b6cd6782ea907aa8cfe1d720e599964110c038f3998e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099095"
---
# <a name="vml-shapetype-element"></a>Elemento ShapeType de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una forma que se puede usar para crear otras formas.

El atributo siguiente modifica un **objeto ShapeType.**



| Atributo                                      | Descripción                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Maestro](msdn-online-vml-master-attribute.md) | Determina si un **objeto ShapeType** es un elemento maestro. |



 

**Comentarios:**

**ShapeType** es idéntico al elemento **Shape,** salvo que no puede hacer referencia a otro **elemento ShapeType.**

Cuando un **elemento Shape** hace referencia a **un shapeType**, **la forma** puede duplicar algunas de las propiedades que ya se han especificado en **shapeType**. En estos casos, los atributos de **shape** invalidan los de **ShapeType**.

El **atributo Type** no se puede usar con **ShapeType.**

Los atributos de posicionamiento CSS (como **Top,** **Left,** etc.) no se pasan a **una forma** desde **un shapeType**.

Para usar este elemento, cree un **shapeType** con un atributo [id.](id-attribute--vml.md) específico. A continuación, **cree una forma** y haga referencia a **ShapeType** con el **atributo Type.** Consulte el [atributo Type](type-attribute--shape--vml.md) para obtener más información.

 

 