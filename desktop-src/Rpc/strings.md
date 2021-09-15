---
title: atributo string (RPC)
description: El atributo \ string\ y la llamada a procedimiento remoto (RPC).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473494"
---
# <a name="string-attribute-rpc"></a>atributo string (RPC)

El atributo string indica que el parámetro es un puntero a una matriz de \[ [](/windows/desktop/Midl/string) \] tipo [char,](/windows/desktop/Midl/char-idl) [byte](/windows/desktop/Midl/byte)o **w \_ char.** Al igual que con una matriz compatible, el tamaño de un parámetro **\[ de \]** cadena se determina en tiempo de ejecución. A diferencia de una matriz compatible, el desarrollador no tiene **\[ \]** que proporcionar la longitud asociada a la matriz: el atributo de cadena indica al código auxiliar que determine el tamaño de la matriz llamando a **strlen**. No **\[ se \] puede** usar un atributo de cadena al mismo tiempo que la longitud \[ [es \_](/windows/desktop/Midl/length-is) \] o el último es \[ [ \_ atributos.](/windows/desktop/Midl/last-is) \]

La **\[ combinación \] de atributos de** cadena de entrada dirige el código auxiliar para pasar la cadena solo del cliente al servidor. La cantidad de memoria asignada en el servidor es la misma que el tamaño de cadena transmitido más uno.

Los \[ [atributos out](/windows/desktop/Midl/out-idl), **string** dirigen el código auxiliar para pasar la cadena solo del servidor \] al cliente. El diseño de llamada por valor del lenguaje C hace que todos los parámetros **\[ de \]** salida sean punteros.

El **\[ parámetro out \]** debe ser un puntero y, de forma predeterminada, todos los parámetros de puntero son punteros de referencia. El puntero de referencia no cambia durante la llamada: apunta a la misma memoria que antes de la llamada. Para los punteros de cadena, la restricción adicional del puntero de referencia significa que el cliente debe asignar suficiente memoria válida antes de realizar la llamada a procedimiento remoto. Los códigos auxiliares transmiten la cadena que los atributos **\[ de cadena out \] indican** en la memoria ya asignada en el lado cliente.

En los temas siguientes se describen los prototipos de parámetros de procedimiento remoto para cadenas:

-   [\[in, out, string \] Prototype](-in-out-string-prototype.md)
-   [\[in, string \] and \[ out, string \] Prototype](-in-string-and-out-string-prototype.md)

 

 