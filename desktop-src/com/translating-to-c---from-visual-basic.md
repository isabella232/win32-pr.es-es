---
title: Traducción a C++ desde Visual Basic
description: Visual Basic controla los punteros implícitamente. En C++, la aplicación es responsable de realizar las operaciones aritméticas de puntero necesarias.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253070"
---
# <a name="translating-to-c-from-visual-basic"></a>Traducción a C++ desde Visual Basic

Visual Basic controla los punteros implícitamente. En C++, la aplicación es responsable de realizar las operaciones aritméticas de puntero necesarias.

De forma predeterminada, Visual Basic parámetros por referencia (como punteros). La palabra clave ByVal especifica los parámetros que están diseñados para pasarse solo por **valor.** Por ejemplo, un parámetro **ByVal** Â **Integer** en Visual Basic equivale **a** un parámetro corto en C++, mientras que un parámetro **ByRef** Â **Integer** en Visual Basic equivale a un **parámetro \*** corto.

Un parámetro que se declara **como** cadena en Visual Basic se declara como puntero a **un BSTR** en C++. Establecer un puntero de cadena **en NULL** en C++ equivale a establecer la cadena en la **constante vbNullString** en Visual Basic. Pasar una cadena de longitud cero ("") a una función diseñada para recibir **NULL** no funciona, ya que pasa un puntero a una cadena de longitud cero en lugar de un puntero cero.

C++ y Visual Basic difieren ligeramente en la forma en que representan las propiedades. En C++, las propiedades se representan como un conjunto de funciones de accessor, una que establece el valor de propiedad y otra que recupera el valor de propiedad. En Visual Basic, las propiedades se representan como un único elemento que se puede usar para recuperar o establecer el valor de propiedad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traducción a C++](translating-to-c--.md)
</dt> </dl>

 

 




