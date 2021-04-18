---
description: Cómo implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Cómo implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536526"
---
# <a name="how-to-implement-iunknown"></a>Cómo implementar IUnknown

Microsoft DirectShow se basa en el modelo de objetos componentes (COM). Si escribe su propio filtro, debe implementarlo como un objeto COM. Las clases base de DirectShow proporcionan un marco desde el que realizar esta tarea. No es necesario usar las clases base, pero puede simplificar el proceso de desarrollo. En este artículo se describen algunos de los detalles internos de los objetos COM y su implementación en las clases base de DirectShow.

En este artículo se supone que sabe cómo programar aplicaciones cliente COM (es decir, que comprende los métodos en **IUnknown**), pero no supone ninguna experiencia previa en el desarrollo de objetos com. DirectShow controla muchos de los detalles del desarrollo de un objeto COM. Si tiene experiencia en el desarrollo de objetos COM, debe leer la sección [uso de CUnknown](using-cunknown.md), que describe la clase base [**CUnknown**](cunknown.md) .

COM es una especificación, no una implementación de. Define las reglas que debe seguir un componente; poner esas reglas en vigor se deja al desarrollador. En DirectShow, todos los objetos se derivan de un conjunto de clases base de C++. Los métodos y constructores de la clase base realizan la mayor parte del trabajo "contabilidad" COM, por ejemplo, mantener un recuento de referencias coherente. Al derivar el filtro de una clase base, se hereda la funcionalidad de la clase. Para utilizar eficazmente las clases base, se necesita una descripción general de cómo implementan la especificación COM.

Este artículo contiene los siguientes temas.

-   [Cómo funciona IUnknown](how-iunknown-works.md)
-   [Usar CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow y COM](directshow-and-com.md)
</dt> </dl>

 

 



