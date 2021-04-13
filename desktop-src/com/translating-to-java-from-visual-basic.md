---
title: Trasladar a Java desde Visual Basic
description: Trasladar a Java desde Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418414"
---
# <a name="translating-to-java-from-visual-basic"></a>Trasladar a Java desde Visual Basic

De forma predeterminada, Visual Basic pasa los parámetros por referencia. Los parámetros que se deben pasar por valor solo se especifican mediante la palabra clave **ByVal**.

Java no admite matrices multidimensionales. Los métodos que aceptan o devuelven matrices multidimensionales no están disponibles en Java.

Java y Visual Basic difieren ligeramente en cómo representan las propiedades. En Java, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad. En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a Java](translating-to-java.md)
</dt> </dl>

 

 




