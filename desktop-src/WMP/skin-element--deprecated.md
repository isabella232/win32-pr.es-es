---
title: Elemento SKIN (en desuso)
description: En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y Reproductor de Windows Media SDK.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (en desuso) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507915"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (en desuso)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Reproductor de Windows Media y Reproductor de Windows Media SDK.

El **elemento SKIN** especifica una dirección URL a un borde.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obligatorio)

Dirección URL de un archivo de borde comprimido con una extensión de nombre de archivo .wmz. Para Reproductor de Windows Media serie 9 o posterior, este valor solo puede hacer referencia a archivos de borde en el disco duro del usuario ubicado en el mismo directorio que la lista de reproducción de metarchivo. Vea el código de ejemplo.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos |
|-----------------|----------|
| Elementos primarios | **Asx**  |
| Elementos secundarios  | Ninguno     |



 

## <a name="remarks"></a>Observaciones

El **elemento SKIN** se usa para crear un borde, que es similar a una máscara, pero se muestra en el área **Reproducción** ahora del modo completo Reproductor de Windows Media. El **elemento SKIN** solo se usa para los bordes, que aparecen dentro del modo completo Reproductor de Windows Media, y no para las máscaras normales, que reemplazan completamente el modo compacto Reproductor de Windows Media.

En un Windows de descarga multimedia (con una extensión de nombre de archivo .wmd), el elemento **SKIN** permite que un borde tenga contenido y vínculo a otros sitios. El Windows de descarga multimedia es un archivo comprimido que contiene un archivo de borde y un metarchivo Windows multimedia. El archivo de borde (con una extensión de nombre de archivo .wmz) está comprimido e incluye un archivo de definición de máscara (con una extensión de nombre de archivo .wms).

Un **elemento SKIN** tiene tres componentes:

-   Una máscara
-   Contenido
-   Metarchivo

Las máscaras incluidas Windows paquetes de descarga multimedia deben tener forma rectangular. La creación de bordes con máscaras que no son rectangulares puede producir resultados inesperados.

## <a name="examples"></a>Ejemplos


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Bordes para Reproductor de Windows Media (en desuso)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





