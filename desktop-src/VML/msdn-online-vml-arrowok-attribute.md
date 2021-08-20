---
title: Atributo ArrowOK de VML
description: Atributo ArrowOK de VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95b8fa7068f55246263e6622527a8ecec17d3351c284a0810cd77b085784aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124977"
---
# <a name="vml-arrowok-attribute"></a>Atributo ArrowOK de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se mostrarán las puntas de flecha. Lectura/escritura **DvTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* arrowok=" *expression* ">

**Sintaxis de script**

*element* .arrowok="*expression*"

*expresión* = *elemento*.arrowok

**Comentarios:**

Si **es False,** la ruta de acceso no tendrá puntas de flecha. El valor predeterminado es **False**. Este atributo invalida todos los demás atributos de la punta de flecha del elemento primario **o del elemento** Stroke.

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



 

 