---
title: Atributo Position (Shape)(VML)
description: Atributo Position (Shape)(VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ffede6653fd865c254392ffbab0bc3feac2f5e0bf51046fc85398306842dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475085"
---
# <a name="position-attribute-shapevml"></a>Atributo Position (Shape)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tipo de posicionamiento utilizado para colocar un elemento. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* style="position: *expression* ">

**Sintaxis de script**

*element* .style.position="*expression*"

*expresión* = *elemento*.style.position

**Comentarios:**

El **atributo Position** es similar al atributo de posición HTML estándar que se usa con las hojas de estilos. 

Estos valores incluyen:



| Value    | Descripción                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static   | Predeterminada. El elemento se coloca según el flujo normal de la página. Los **atributos Top** e **Left** se omiten. Si el objeto está delimitado en línea, lo que solo se produce en Microsoft Word, se usa este valor. |
| absolute | El elemento se coloca en relación con el elemento primario, utilizando los **atributos Top** **e Left.** Este valor lo usan los Microsoft Word y Microsoft Excel flotantes, y Microsoft PowerPoint diapositivas.                  |
| relative | El elemento se coloca según el flujo normal de la página, pero se usan los atributos **Superior** **e** Izquierdo. La superposición de elementos superpuestos se rige por el **atributo Z-Index.**                       |



 

*Atributo estándar de VML*

**Ejemplo**

La posición del rectángulo se muestra con el *estilo* relativo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo position](/previous-versions/bb264090(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 