---
title: Punteros y RPC
description: Es muy eficaz usar punteros como parámetros de la función de C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903720"
---
# <a name="pointers-and-rpc"></a>Punteros y RPC

Es muy eficaz usar punteros como parámetros de la función de C. El puntero solo cuesta unos pocos bytes y se puede usar para tener acceso a una gran cantidad de memoria. Sin embargo, en una aplicación distribuida, los procedimientos de cliente y servidor residen en diferentes espacios de direcciones: pueden estar en equipos diferentes. Por lo tanto, el cliente y el servidor no suelen tener acceso al mismo espacio de memoria.

Cuando uno de los parámetros del procedimiento remoto es un puntero a un objeto, el cliente debe transmitir una copia de ese objeto y su puntero al servidor. Si el procedimiento remoto modifica el objeto a través de su puntero, el servidor devuelve el puntero y su copia modificada.

MIDL ofrece atributos de puntero para minimizar la cantidad de sobrecarga necesaria y el tamaño de la aplicación. En esta sección se describen el propósito y los usos de los atributos de puntero de MIDL. También se muestra información sobre el control de puntero en las aplicaciones RPC. Se divide en los siguientes temas:

-   [Tipos de punteros](kinds-of-pointers.md)
-   [Punteros y asignación de memoria](pointers-and-memory-allocation.md)
-   [Tipos de puntero predeterminados](default-pointer-types.md)
-   [Herencia de tipos de atributos de puntero](pointer-attribute-type-inheritance.md)

 

 




