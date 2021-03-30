---
title: atributo de cadena (RPC)
description: El atributo \ String \ y la llamada a procedimiento remoto (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995531"
---
# <a name="string-attribute-rpc"></a>atributo de cadena (RPC)

El \[ atributo de [cadena](/windows/desktop/Midl/string) \] indica que el parámetro es un puntero a una matriz de tipo [Char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte)o **w \_ Char**. Al igual que con una matriz compatible, el tamaño de un parámetro de **\[ cadena \]** se determina en tiempo de ejecución. A diferencia de una matriz compatible, el desarrollador no tiene que proporcionar la longitud asociada a la matriz; el atributo de **\[ cadena \]** indica al código auxiliar que determine el tamaño de la matriz mediante una llamada a **strlen**. No se puede usar un atributo de **\[ cadena \]** al mismo tiempo que la \[ [longitud \_ es](/windows/desktop/Midl/length-is) \] o los \[ atributos [ \_ Last](/windows/desktop/Midl/last-is) \] .

La combinación **\[ de atributo \] de cadena** indica al código auxiliar que solo debe pasar la cadena del cliente al servidor. La cantidad de memoria asignada en el servidor es igual que el tamaño de la cadena transmitida más una.

Los \[ atributos de **cadena** [out](/windows/desktop/Midl/out-idl) \] indican que el código auxiliar solo debe pasar la cadena del servidor al cliente. El diseño de llamada por valor del lenguaje C insiste en que todos los parámetros **\[ out \]** deben ser punteros.

El parámetro **\[ out \]** debe ser un puntero y, de forma predeterminada, todos los parámetros de puntero son punteros de referencia. El puntero de referencia no cambia durante la llamada, sino que apunta a la misma memoria que antes de la llamada. En el caso de los punteros de cadena, la restricción adicional del puntero de referencia significa que el cliente debe asignar suficiente memoria válida antes de hacer la llamada a procedimiento remoto. El código auxiliar transmite la cadena de **\[ salida, \]** los atributos de cadena indican en la memoria ya asignada en el lado cliente.

En los temas siguientes se describen los prototipos de parámetro de procedimiento remoto para las cadenas:

-   [\[in, out, prototipo de cadena \]](-in-out-string-prototype.md)
-   [\[in, String \] y \[ out, prototipo de cadena \]](-in-string-and-out-string-prototype.md)

 

 