---
title: Inercia
description: En esta sección se explica la inercia de Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Touch, inercia
- inercia, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075207"
---
# <a name="inertia"></a>Inercia

En esta sección se explica la inercia de Windows Touch.

La API de inercia incluida en Windows 7 permite el comportamiento de objetos coherentes en las aplicaciones táctiles de Windows al proporcionar un modelo físico simple. La inercia se habilita mediante el procesador de inercia, una clase que encapsula la funcionalidad. El procesador de inercia funciona mediante el procesamiento de eventos que se le pasan cuando las manipulaciones de objetos finalizan y controlan las trayectorias de objeto de una manera coherente con otras aplicaciones. Tenga en cuenta que el procesador de inercia está estrechamente acoplado al procesador de manipulación para simplificar la adición de compatibilidad de inercia a las aplicaciones que usan manipulaciones. De hecho, el procesador de inercia genera los mismos eventos que el procesador de manipulación. En la siguiente sección se explica cómo empezar a usar la inercia.



| Sección                                                                      | Descripción                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Mecánica de inercia](inertia-mechanics.md)                                   | Explica los conceptos básicos de los cálculos de inercia.                                                                             |
| [Controlar la inercia en código no administrado](handling-inertia-in-unmanaged-code.md) | Explica cómo usar la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para controlar la inercia en el código no administrado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones e inercia](manipulation-and-inertia.md)
</dt> </dl>

 

 




