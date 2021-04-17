---
title: Elemento SKIN (obsoleto)
description: En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (obsoleto) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660885"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (obsoleto)

En esta página se documenta una característica que puede no estar disponible en versiones futuras de Windows Media Player y el SDK de Windows Media Player.

El elemento **Skin** especifica una dirección URL a un borde.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obligatorio)

Dirección URL de un archivo de borde comprimido con una extensión de nombre de archivo. WMZ. En Windows Media Player serie 9 o versiones posteriores, este valor solo puede hacer referencia a los archivos de borde del disco duro del usuario ubicado en el mismo directorio que la lista de reproducción del metarchivo. Vea el código de ejemplo.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos |
|-----------------|----------|
| Elementos primarios | **ASX**  |
| Elementos secundarios  | Ninguno     |



 

## <a name="remarks"></a>Observaciones

El elemento **Skin** se usa para crear un borde, que es similar a una máscara, pero que se muestra en el área **reproducción en curso** del Media Player de Windows en modo completo. El elemento **Skin** solo se usa para los bordes, que aparecen dentro del Media Player de Windows en modo completo y no para las máscaras normales, que reemplazan por completo a la Media Player de Windows en modo compacto.

En un paquete de descarga de Windows Media (con la extensión de nombre de archivo. WMD), el elemento de **máscara** habilita un borde para tener contenido y vincular a otros sitios. El paquete de descarga de Windows Media es un archivo comprimido que contiene un archivo de borde y un metarchivo de Windows Media. El archivo de borde (con la extensión de nombre de archivo. WMZ) se comprime e incluye un archivo de definición de máscara (con una extensión de nombre de archivo. WMS).

Un elemento **Skin** tiene tres componentes:

-   Una máscara
-   Algún contenido
-   Un metarchivo

Las máscaras que se incluyen con los paquetes de descarga de Windows Media deben ser rectangulares. La creación de bordes con máscaras que no son rectangulares puede producir resultados inesperados.

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
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Bordes de Media Player de Windows (desusado)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





