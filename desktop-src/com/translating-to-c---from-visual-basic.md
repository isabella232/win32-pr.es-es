---
title: Traducir a C++ desde Visual Basic
description: Visual Basic controla los punteros implícitamente. En C++, la aplicación es responsable de realizar cualquier aritmética de puntero necesaria.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268733"
---
# <a name="translating-to-c-from-visual-basic"></a>Traducir a C++ desde Visual Basic

Visual Basic controla los punteros implícitamente. En C++, la aplicación es responsable de realizar cualquier aritmética de puntero necesaria.

De forma predeterminada, Visual Basic pasa los parámetros por referencia (como punteros). Los parámetros que se deben pasar por valor solo se especifican mediante la palabra clave **ByVal**. Por ejemplo, un **parámetro ByVal** â  **integer** en Visual Basic es equivalente a un **parámetro Short** en C++, mientras que un parámetro de  **tipo entero** **ByRef** en Visual Basic es equivalente a un parámetro **Short \*** .

Un parámetro declarado **como String** en Visual Basic se declara como un puntero a un **BSTR** en C++. Establecer un puntero de cadena en **null** en C++ es equivalente a establecer la cadena en la constante **vbNullString** en Visual Basic. Pasar una cadena de longitud cero ("") a una función diseñada para recibir **null** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de un puntero cero.

C++ y Visual Basic difieren ligeramente en la forma en que representan las propiedades. En C++, las propiedades se representan como un conjunto de funciones de descriptor de acceso, una que establece el valor de propiedad y otra que recupera el valor de propiedad. En Visual Basic, las propiedades se representan como un único elemento que se puede utilizar para recuperar o establecer el valor de la propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducir a C++](translating-to-c--.md)
</dt> </dl>

 

 




