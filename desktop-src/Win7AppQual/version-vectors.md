---
description: Un vector de versión procesa los comentarios condicionales en una página web HTML. Es decir, los vectores de versión permiten crear marcado basado en la versión del explorador.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vectores de versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ba3fb77d13ce6aa08a095f4ae95e88c1ffaecf57251b7d9ad718f51be3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328611"
---
# <a name="version-vectors"></a>Vectores de versión

Un *vector de versión* procesa los comentarios condicionales en una página web HTML. Es decir, los vectores de versión permiten crear marcado basado en la versión del explorador.

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



En este caso, si Windows Internet Explorer versión del explorador es al menos 5.5, el párrafo correspondiente se muestra en la página web. Aunque la primera condición de este ejemplo ilustra la función de los comentarios condicionales, estos comentarios no se usan normalmente para mostrar marcado como la primera condición. En su lugar, los comentarios condicionales restantes del ejemplo anterior son más comunes. En estos comentarios restantes, los comentarios condicionales usan una hoja de estilos diferente para cada versión diferente del explorador.

En el ejemplo de código anterior también se comprueba la igualdad de Microsoft Internet Explorer 6 y Windows Internet Explorer 7. Pero para Windows Internet Explorer 8, en el ejemplo se usa el operador gte (mayor o igual que). Este operador ayuda a probar el futuro del ejemplo para que se use la versión más compatible con los estándares de la hoja de estilos cuando se libera una nueva versión del explorador (en lugar de usar una hoja de estilos incorrecta o ninguna hoja de estilos). Las aplicaciones existentes a menudo no tienen en cuenta una versión de Internet Explorer pasados 7 (o la versión más reciente de Internet Explorer para la que se ha creado el sitio). Para obtener más información sobre los vectores de versión, vea [Vectores de versión](/previous-versions/cc817577(v=msdn.10)) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



