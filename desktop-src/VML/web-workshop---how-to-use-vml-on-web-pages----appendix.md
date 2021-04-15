---
title: Apéndice (VML)
description: En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Web Workshop, espacios de nombres
- Web Workshop, estilos de comportamiento
- diseñar páginas web, espacios de nombres
- diseñar páginas web, estilos de comportamiento
- Lenguaje de marcado de vectores (VML), espacios de nombres
- VML (Lenguaje de marcado de vectores), espacios de nombres
- gráficos vectoriales, espacios de nombres
- Lenguaje de marcado de vectores (VML), estilos de comportamiento
- VML (Lenguaje de marcado de vectores), estilos de comportamiento
- gráficos vectoriales, estilos de comportamiento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421824"
---
# <a name="appendix-vml"></a>Apéndice (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Para que los exploradores sepan cómo entregar los datos a un procesador específico de VML, debe escribir información como espacios de nombres y estilos de comportamiento. Después, puede usar VML para escribir gráficos en la `<BODY>` región.

En este tema:

-   [Espacios de nombres](#namespaces)
-   [Estilos de comportamiento](#behavior-styles)

## <a name="namespaces"></a>Espacios de nombres

Un mecanismo XML indica el espacio de nombres del que procede un elemento. Si cambia del análisis en HTML al análisis en XML, este mecanismo indica el modificador en HTML.

Pregunte al expendedor del procesador VML qué información es necesaria para el espacio de nombres XML.

Si utiliza Microsoft Internet Explorer para representar VML, escriba siempre la siguiente línea en la `<HTML>` etiqueta:


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Esta información indica a Internet Explorer que cambie al espacio de nombres "urn: schemas-microsoft-com: VML" al analizar una etiqueta XML con un prefijo `v:` y a entregar los datos resultantes al procesador VML.

[![volver ](images/top.gif) al principio hacia arriba](#top)

## <a name="behavior-styles"></a>Estilos de comportamiento

VML se define en Microsoft Internet Explorer como un comportamiento predeterminado.

Para representar VML, escriba siempre las líneas siguientes en la `<HEAD>` región:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML se implementa en Internet Explorer a través de VGX.DLL. Si la instalación inicial del explorador no incluía el comportamiento de VML, puede que tenga que agregarlo como una opción. No es necesario agregar una `<object>` etiqueta.

 

 
