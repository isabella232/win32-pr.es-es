---
description: Un vector de versión procesa los comentarios condicionales en una página web HTML. Es decir, los vectores de versión permiten crear el marcado en función de la versión del explorador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vectores de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361708"
---
# <a name="version-vectors"></a>Vectores de versión

Un *Vector de versión* procesa los comentarios condicionales en una página web HTML. Es decir, los vectores de versión permiten crear el marcado en función de la versión del explorador.

Tenga en cuenta el siguiente código de ejemplo.


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



En este caso, si la versión del explorador de Windows Internet Explorer es al menos 5,5, el párrafo correspondiente se muestra en la Página Web. Aunque la primera condición de este ejemplo muestra la función de los comentarios condicionales, estos comentarios no se suelen usar para mostrar el marcado como la primera condición. En su lugar, los comentarios condicionales restantes en el ejemplo anterior son más comunes. En estos comentarios restantes, los comentarios condicionales usan una hoja de estilos diferente para cada versión diferente del explorador.

En el ejemplo de código anterior también se comprueba la igualdad de Microsoft Internet Explorer 6 y Windows Internet Explorer 7. Pero para Windows Internet Explorer 8, el ejemplo utiliza el operador de GTE (mayor o igual que). Este operador ayuda a probar en el futuro el ejemplo para que se use la versión más conforme a los estándares de la hoja de estilos cuando se lance una nueva versión del explorador (en lugar de usar la hoja de estilos equivocada o ninguna hoja de estilos). Las aplicaciones existentes no suelen tener en cuenta una versión de Internet Explorer anterior 7 (o la versión más reciente de Internet Explorer para la que se ha creado el sitio). Para obtener más información acerca de los vectores de versión, consulte [vectores de versión](/previous-versions/cc817577(v=msdn.10)) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



