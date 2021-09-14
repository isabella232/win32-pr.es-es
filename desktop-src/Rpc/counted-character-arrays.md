---
title: Matrices de caracteres con recuento
description: El atributo \ size is\ indica el límite superior de la matriz, mientras que el atributo \ length is\ indica el número de elementos de matriz que se \_ \_ transmitirán.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259852"
---
# <a name="counted-character-arrays"></a>Matrices de caracteres con recuento

El atributo size is indica el límite superior de la matriz, mientras que el atributo length is indica el número de elementos de \[ [ \_ ](/windows/desktop/Midl/size-is) \] \[ [ \_ ](/windows/desktop/Midl/length-is) \] matriz que se transmitirán. Además de la matriz, el prototipo de procedimiento remoto debe incluir variables que representen la longitud o el tamaño que determinen los elementos de la matriz transmitidos (pueden ser parámetros independientes o incluirse con la cadena en una estructura). Estos atributos se pueden usar con matrices de caracteres anchos o de un solo byte, tal como lo harían con matrices de otros tipos.

La información de esta sección describe prototipos de parámetros de procedimiento remoto para matrices de caracteres. Se divide en los temas siguientes:

-   [\[in, out, size \_ is \] Prototype](-in-out-size-is-prototype.md)
-   [\[in, size \_ is and out, size \_ is \] Prototype](-in-size-is-and-out-size-is-prototype.md)

 

 