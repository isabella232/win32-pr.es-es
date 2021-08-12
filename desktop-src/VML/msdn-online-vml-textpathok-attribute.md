---
title: Atributo TextPathOK de VML
description: Atributo TextPathOK de VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2c14d613df36c314dea75275a4d60fe8792d6dea644ef2595422e74a73dc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597459"
---
# <a name="vml-textpathok-attribute"></a>Atributo TextPathOK de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará una ruta de acceso de texto. Lectura/escritura **DvTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* textpathok=" *expression* ">

**Sintaxis de script**

*elemento* . textpathok= "*expression*"

*expresión* = *elemento*. textpathok

**Comentarios:**

Si **es False,** la ruta de acceso no puede tener una ruta de acceso de texto. El valor predeterminado es **False**. Debe tener este atributo establecido en **True para** mostrar texto en una ruta de acceso.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un trazado de texto. El texto "Hello VML" se muestra a lo largo de una curva con forma de sonrisa.


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 