---
title: Matrices de caracteres contables
description: El atributo \ size \_ es \ indica el límite superior de la matriz mientras que el atributo \ length \_ es \ indica el número de elementos de matriz que se van a transmitir.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487986"
---
# <a name="counted-character-arrays"></a>Matrices de caracteres contables

El \[ [atributo \_ size](/windows/desktop/Midl/size-is) \] indica el límite superior de la matriz mientras que la \[ [longitud \_ es](/windows/desktop/Midl/length-is) \] Attribute indica el número de elementos de matriz que se van a transmitir. Además de la matriz, el prototipo de procedimiento remoto debe incluir las variables que representan la longitud o el tamaño que determinan los elementos de la matriz transmitida (pueden ser parámetros independientes o agrupados con la cadena en una estructura). Estos atributos se pueden usar con matrices de caracteres anchos o de un solo byte, tal y como lo harían con matrices de otros tipos.

La información de esta sección describe los prototipos de parámetros de procedimientos remotos para las matrices de caracteres. Se divide en los siguientes temas:

-   [\[in, out, el tamaño \_ es \] prototype](-in-out-size-is-prototype.md)
-   [\[en, el tamaño \_ es y fuera, el tamaño \_ es \] prototipo](-in-size-is-and-out-size-is-prototype.md)

 

 