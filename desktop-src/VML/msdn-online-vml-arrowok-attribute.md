---
title: Atributo ArrowOK de VML
description: Atributo ArrowOK de VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420942"
---
# <a name="vml-arrowok-attribute"></a>Atributo ArrowOK de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se mostrarán las puntas de flecha. Lectura/escritura **VgTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *Element* arrowok = " *expresión* " >

**Sintaxis de script**

*Element* . arrowok = "*expresión*"

*expresión* = de *elemento*. arrowok

**Comentarios:**

Si **es false**, la ruta de acceso no tendrá puntas de flecha. El valor predeterminado es **False**. Este atributo invalida todos los demás atributos de la punta de flecha en el elemento primario o de **trazo** .

*Atributo estándar de VML*

**Ejemplo**

La ruta de acceso no tendrá una punta de flecha.


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 