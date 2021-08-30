---
title: Atributo ShadowOK de VML
description: Atributo ShadowOK de VML
ms.assetid: 88400bf5-f41c-4495-a5d0-9b35c1cae9f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce851a8e6d6bf458213521248cee05d3beb3d32dd6b235b93dd666a4c75051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099105"
---
# <a name="vml-shadowok-attribute"></a>Atributo ShadowOK de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará una sombra. Lectura/escritura **DvTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* shadowok=" *expression* ">

**Sintaxis de script**

*element* .shadowok="*expression*"

*expresión* = *elemento*.shadowok

**Comentarios:**

Si **es False**, la ruta de acceso no puede tener una sombra. El valor predeterminado es **True**. Este atributo invalida todos los demás atributos de sombra en el elemento primario o **shadow.**

*Atributo estándar de VML*

**Ejemplo**

La forma no tendrá una sombra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True" offset="5pt,5pt" color="blue"/>
   <v:path id= "myPath" shadowok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 