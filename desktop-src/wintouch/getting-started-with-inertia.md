---
title: Inercia
description: En esta sección se explica la inercia de Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Táctil, inercia
- inercia, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ff1fd58d52ba73d758254c1dac1e8952df30b836b68ef12b022a29ceafc694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709815"
---
# <a name="inertia"></a>Inercia

En esta sección se explica la inercia de Windows Touch.

La API de inercia incluida en Windows 7 permite un comportamiento coherente de los objetos en Windows Touch al proporcionar un modelo físico simple. La inercia se habilita mediante el procesador de inercia, una clase que encapsula la funcionalidad. El procesador de inercia funciona procesando eventos que se le pasan cuando finalizan las manipulaciones de objetos y controlando las representaciones de objetos de forma coherente con otras aplicaciones. Tenga en cuenta que el procesador de inercia está estrechamente acoplado al procesador de manipulación para simplificar la adición de compatibilidad con la inercia a las aplicaciones que usan manipulaciones. De hecho, el procesador de inercia genera los mismos eventos que el procesador de manipulación. En la sección siguiente se explica cómo empezar a trabajar con la inercia.



| Sección                                                                      | Descripción                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Mecanismos de inercia](inertia-mechanics.md)                                   | Explica los conceptos básicos de los cálculos de inercia.                                                                             |
| [Control de la inercia en código no administrado](handling-inertia-in-unmanaged-code.md) | Explica cómo usar la interfaz [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) para controlar la inercia en código no administrado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Manipulaciones e inercia](manipulation-and-inertia.md)
</dt> </dl>

 

 




