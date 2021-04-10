---
description: Combinación alfa
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Combinación alfa (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152565"
---
# <a name="alpha-blending-directshow"></a>Combinación alfa (DirectShow)

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

En este artículo se describe la combinación alfa en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).

Alfa mide la transparencia de un píxel o imagen. En vídeo RGB sin comprimir de 32 bits, cuatro componentes definen cada píxel: un canal alfa (A) y tres componentes de color (RGB). Un píxel con un valor alfa de cero es completamente transparente. Un píxel con un valor alfa de 255 es opaco. Entre estos valores, el píxel tiene varios grados de transparencia.

DirectShow define dos tipos de medios para vídeo RGB de 32 bits:

-   **MEDIASUBTYPE \_ ARGB32**: el vídeo es RGB de 32 bits con un canal alfa válido.
-   **MEDIASUBTYPE \_ RGB32**: los píxeles son de 32 bits, pero el canal alfa no es necesariamente válido.

Para realizar la combinación alfa en DES, establezca el tipo de medio sin comprimir del grupo de vídeos en MEDIASUBTYPE \_ ARGB32. En C++, llame al método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) . En el formato XTL, al establecer el atributo [**bitdepth**](bitdepth-attribute.md) del elemento [**Group**](group-element.md) en 32 también se consigue esto.

A continuación, necesita datos de vídeo que contengan un canal alfa. Hay varias opciones:

-   Puede usar un archivo AVI que ya tiene vídeo RGB de 32 bits con datos alfa. Actualmente, no se admite Alpha para los archivos de código fuente MPEG o Microsoft Windows Media Format (WMF).
-   DES admite archivos de mapa de bits de 32 bits (. bmp) y Targa (. TGA) con datos alfa.
-   Puede escribir un filtro de origen personalizado que cree datos RGB de 32 bits con alfa. El tipo de medio de salida debe ser **MEDIASUBTYPE \_ ARGB32**. Use el filtro como el subobjeto en un objeto de origen de la escala de tiempo.

Si el origen de vídeo no tiene alfa, puede usar un efecto que cree datos alfa. El [efecto](alpha-setter-effect.md) establecedor alfa establece el canal alfa de la imagen completa en un valor constante. Para variar el alfa a lo largo del tiempo, use la interfaz [**IPropertySetter**](ipropertysetter.md) con el efecto del establecedor alfa. El origen original no tiene que ser de 32 bits, siempre que el tipo de medio sin comprimir del grupo sea **MEDIASUBTYPE \_ ARGB32**.

Por último, pase el vídeo a un efecto o transición que realice la combinación alfa. La [transición del compositor](compositor-transition.md) realiza la combinación alfa y la transición de la [clave](key-transition.md) puede clave mediante el valor alfa.

En el siguiente proyecto de XTL de ejemplo se realiza la combinación alfa:


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



