---
title: ID (atributo) (VML)
description: ID (atributo) (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487902"
---
# <a name="id-attribute-vml"></a>ID (atributo) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Proporciona un identificador único para un elemento. Lectura/escritura **Cadena**.

**Se aplica a**

Todos los elementos VML.

**Sintaxis de etiquetas**

<v: *ElementName* ID = " *idname* " >

**Sintaxis de script**

*ElementName* . ID = " *idname* "

*expresión* = de *ElementName*. ID

**Comentarios:**

Use **ID** para hacer referencia a un elemento específico. Una vez que haya creado una forma y dado un identificador, puede utilizar el nombre de identificador cuando desee manipular el elemento.

El **identificador** es necesario para usar el elemento [TipoForma](msdn-online-vml-shapetype-element.md) .

Cuando Microsoft Office genera VML, si se asigna un nombre de modelo de objetos a la forma, **ID** se establece en este nombre. Si no se establece el nombre del modelo de objetos, el nombre se genera mediante el *SPID* (ID. de forma interna) más un prefijo (S para la forma, M para la forma maestra, T para TipoForma).

*Atributo estándar de VML*.

**Ejemplo**

Para cambiar los atributos de una forma, primero debe proporcionar un identificador a la forma; por ejemplo, "trirect".


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



[Ejemplo del atributo ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 