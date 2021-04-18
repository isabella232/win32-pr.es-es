---
title: Contención/delegación
description: El mecanismo más común para la reutilización de objetos en COM es la contención o delegación.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357692"
---
# <a name="containmentdelegation"></a>Contención/delegación

El mecanismo más común para la reutilización de objetos en COM es la *contención o delegación*. Este tipo de reutilización es un concepto conocido que se encuentra en la mayoría de los lenguajes y sistemas orientados a objetos. El objeto externo, que necesita hacer uso del objeto interno, actúa como cliente de objeto para el objeto interno. El objeto externo "contiene" el objeto interno y, cuando el objeto externo requiere los servicios del objeto interno, el objeto externo delega explícitamente la implementación a los métodos del objeto interno. Es decir, el objeto externo utiliza los servicios del objeto interno para implementarse a sí mismo.

No es necesario que los objetos externos e internos admitan las mismas interfaces, aunque ciertamente es razonable contener un objeto que implementa una interfaz que el objeto externo no e implementar los métodos del objeto externo simplemente como llamadas a los métodos correspondientes en el objeto interno. Sin embargo, cuando la complejidad de los objetos externos e internos difiere en gran medida, el objeto externo puede implementar algunos de los métodos de sus interfaces mediante la delegación de llamadas a métodos de interfaz implementados en el objeto interno.

Es fácil implementar la contención para un objeto externo. El objeto externo crea los objetos internos que necesita usar como cualquier otro cliente. Esto no es nada nuevo: el proceso es como un objeto de C++ que contiene un objeto de cadena de C++ que usa para realizar determinadas funciones de cadena, incluso si el objeto externo no se considera un objeto de cadena por su derecho. A continuación, con su puntero al objeto interno, una llamada a un método en el objeto externo genera una llamada a un método de objeto interno.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Agregación](aggregation.md)
</dt> </dl>

 

 




