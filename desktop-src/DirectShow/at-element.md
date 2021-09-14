---
description: El elemento at define el valor de un elemento param en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el parámetro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at (Elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162234"
---
# <a name="at-element"></a>at (Elemento)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `at` elemento define el valor de un elemento [**param**](param-element.md) en un momento determinado, en relación con el inicio de la transición o el efecto que contiene el parámetro . El `at` elemento hace que el parámetro salte repentinamente al nuevo valor en el momento dado. Para una progresión suave a un nuevo valor, use el [**elemento**](linear-element.md) lineal.

## <a name="attributes"></a>Atributos

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Información de elementos primarios y secundarios



| Etiqueta | Value |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | None                           |



 

## <a name="examples"></a>Ejemplos


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



