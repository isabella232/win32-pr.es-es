---
title: Atributo FillOK de VML
description: Atributo FillOK de VML
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346e4499e8c9a0ba390936a61e8c1cd1b4f36c5b115904cfdaee24f4c29ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124825"
---
# <a name="vml-fillok-attribute"></a>Atributo FillOK de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará un relleno. Lectura/escritura **DvTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* fillok=" *expression* ">

**Sintaxis de script**

*element* .fillok="*expression*"

*expresión* = *elemento*.fillok

**Comentarios:**

Si **es False**, no se puede rellenar la ruta de acceso. El valor predeterminado es **True**. Este atributo invalida todos los demás atributos de relleno en el elemento primario **o en el elemento Fill.**

*Atributo estándar de VML*

**Ejemplo**

La ruta de acceso no se rellenará.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 