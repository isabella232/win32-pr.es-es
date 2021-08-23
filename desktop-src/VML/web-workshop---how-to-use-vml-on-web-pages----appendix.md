---
title: Apéndice (VML)
description: En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Taller web, espacios de nombres
- Taller web, estilos de comportamiento
- diseñar páginas web, espacios de nombres
- diseñar páginas web, estilos de comportamiento
- Lenguaje de marcado de vectores (VML),namespaces
- VML (Lenguaje de marcado de vectores),namespaces
- gráficos vectoriales, espacios de nombres
- Lenguaje de marcado de vectores (VML),estilos de comportamiento
- VML (Lenguaje de marcado de vectores),estilos de comportamiento
- gráficos vectoriales, estilos de comportamiento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640de79138adcc345d4352ead814195007b88e0714a0f89816819d545e6e1ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512615"
---
# <a name="appendix-vml"></a>Apéndice (VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Para que los exploradores sepan cómo entregar datos a un procesador específico de VML, debe escribir cierta información, como espacios de nombres y estilos de comportamiento. A continuación, puede usar VML para escribir gráficos en la `<BODY>` región.

En este tema:

-   [Espacios de nombres](#namespaces)
-   [Estilos de comportamiento](#behavior-styles)

## <a name="namespaces"></a>Espacios de nombres

Un mecanismo XML indica el espacio de nombres del que procede un elemento. Si pasa de analizar en HTML a analizar en XML, este mecanismo indica el modificador dentro de HTML.

Pregunte al vendedor del procesador VML qué información es necesaria para el espacio de nombres XML.

Si usa Microsoft Internet Explorer para representar VML, escriba siempre la siguiente línea en la `<HTML>` etiqueta :


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Esta información indica a Internet Explorer cambiar al espacio de nombres "urn:schemas-microsoft-com:vml" al analizar una etiqueta XML con un prefijo y entregar los datos resultantes al procesador `v:` VML.

[![volver a la parte ](images/top.gif) superior Atrás a la parte superior](#top)

## <a name="behavior-styles"></a>Estilos de comportamiento

VML se define en Microsoft Internet Explorer comportamiento predeterminado.

Para representar VML, escriba siempre las siguientes líneas en la `<HEAD>` región:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML se implementa en Internet Explorer a VGX.DLL. Si la instalación inicial del explorador no incluye el comportamiento de VML, es posible que tenga que agregarlo como una opción. No es necesario agregar una `<object>` etiqueta.

 

 
