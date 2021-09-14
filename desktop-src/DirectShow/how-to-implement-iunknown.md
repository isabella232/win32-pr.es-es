---
description: Cómo implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Cómo implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169906"
---
# <a name="how-to-implement-iunknown"></a>Cómo implementar IUnknown

Microsoft DirectShow se basa en el modelo de objetos componentes (COM). Si escribe su propio filtro, debe implementarlo como un objeto COM. Las DirectShow base proporcionan un marco desde el que hacer esto. El uso de las clases base no es necesario, pero puede simplificar el proceso de desarrollo. En este artículo se describen algunos de los detalles internos de los objetos COM y su implementación en las DirectShow base.

En este artículo se da por supuesto que sabe cómo programar aplicaciones cliente COM, es decir, que comprende los métodos de **IUnknown,** pero no supone ninguna experiencia previa en el desarrollo de objetos COM. DirectShow muchos de los detalles del desarrollo de un objeto COM. Si tiene experiencia en el desarrollo de objetos COM, debe leer la sección Using CUnknown (Uso de [CUnknown),](using-cunknown.md)que describe la clase base [**CUnknown.**](cunknown.md)

COM es una especificación, no una implementación. Define las reglas que debe seguir un componente; Poner esas reglas en vigor se deja al desarrollador. En DirectShow, todos los objetos derivan de un conjunto de clases base de C++. Los constructores y métodos de clase base hacen la mayor parte del trabajo de "contabilidad" COM, como mantener un recuento de referencias coherente. Al derivar el filtro de una clase base, hereda la funcionalidad de la clase . Para usar las clases base de forma eficaz, necesita una comprensión general de cómo implementan la especificación COM.

Este artículo contiene los temas siguientes.

-   [Funcionamiento de IUnknown](how-iunknown-works.md)
-   [Uso de CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow y COM](directshow-and-com.md)
</dt> </dl>

 

 



