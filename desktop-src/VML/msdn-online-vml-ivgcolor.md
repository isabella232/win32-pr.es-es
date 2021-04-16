---
title: IVgColor VML
description: IVgColor VML
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d4800fbb99557acfbd3fd6e0dbbd893f30158f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487894"
---
# <a name="vml-ivgcolor"></a>IVgColor VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica un color.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>String. Representación de texto del color. Se admiten los siguientes tipos de colores con nombre:
<ul>
<li>Negro (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Gris (#808080)</li>
<li>Blanco (#FFFFFF)</li>
<li>Granate (#800000)</li>
<li>Rojo (#FF0000)</li>
<li>Púrpura (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lima (#00FF00)</li>
<li>Oliva (#808000)</li>
<li>Amarillo (#FFFF00)</li>
<li>Navy (#000080)</li>
<li>Blue (#0000FF)</li>
<li>Verde azulado (#008080)</li>
<li>Aguamarina (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgColorType. Tipo de color. Uno de los siguientes tipos:
<ul>
<li>Mixto</li>
<li>RGB</li>
<li>Scheme</li>
<li>con nombre</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. Valor RGB (<strong>Long</strong>) del color. Solo es válido si el tipo es &quot; <strong>RGB</strong> &quot; .</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Entero</strong>. Componente rojo del color. Puede oscilar entre 0 y 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Entero</strong>. Componente verde del color. Puede oscilar entre 0 y 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Entero</strong>. Componente azul del color. Puede oscilar entre 0 y 255.</td>
</tr>
</tbody>
</table>



 

 

 