---
title: Elemento TipoForma de VML
description: Elemento TipoForma de VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271270"
---
# <a name="vml-shapetype-element"></a>Elemento TipoForma de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una forma que se puede utilizar para crear otras formas.

El atributo siguiente modifica un **TipoForma**.



| Atributo                                      | Descripción                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Maestra](msdn-online-vml-master-attribute.md) | Determina si **TipoForma** es un elemento principal. |



 

**Comentarios:**

**TipoForma** es idéntico al elemento **Shape** , pero no puede hacer referencia a otro elemento **TipoForma** .

Cuando un elemento de **forma** hace referencia a un **TipoForma**, la **forma** puede duplicar algunas de las propiedades que ya se han especificado en el **TipoForma**. En estos casos, los atributos de la **forma** invalidan los del **TipoForma**.

El atributo de **tipo** no se puede usar con **TipoForma**.

Los atributos de colocación de CSS (como **Top**, **left**, etc.) no se pasan a una **forma** de **TipoForma**.

Para usar este elemento, cree un **TipoForma** con un atributo de [identificador](id-attribute--vml.md) específico. A continuación, cree una **forma** y haga referencia al **TipoForma** con el atributo **Type** . Vea el atributo [Type](type-attribute--shape--vml.md) para obtener más información.

 

 