---
title: Elemento ASX
description: El elemento ASX define un archivo como un metarchivo.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Elemento ASX de Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700063"
---
# <a name="asx-element"></a>Elemento ASX

El elemento **ASX** define un archivo como un metarchivo.

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>Atributos

`VERSION` (obligatorio)

Número decimal que representa el número de versión de la sintaxis del metarchivo. Establezca en 3 o 3,0.

**PREVIEWMODE** (opcional)

Valor que indica si Windows Media Player entra en el modo de vista previa antes de reproducir el primer clip.

Debe ser uno de los valores siguientes.



| Value | Descripción                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| SÍ   | Windows Media Player entra en el modo de vista previa antes de reproducir el primer clip.                            |
| No    | Valor predeterminado. Windows Media Player no entra en el modo de vista previa antes de reproducir el primer clip. |



 

**BANNERBAR** (opcional)

Valor que indica si Windows Media Player Reserva espacio para un gráfico de banner.

Debe ser uno de los valores siguientes.



| Value | Descripción                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | Valor predeterminado. Windows Media Player Reserva espacio para la barra de pancarta solo cuando una parte de contenido incluye una.                       |
| FIXED | Windows Media Player reserva un espacio fijo para un gráfico de banner para cada fragmento de contenido reproducido, independientemente de si hay un banner asociado. |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy       | Elementos                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios | Ninguno. El elemento **ASX** debe ser el primer elemento de cada metarchivo.                                                                                                 |
| Elementos secundarios  | **abstract**, **Author**, **banner**, **base**, **Copyright**, **entry**, **ENTRYREF**, **Event**, **MOREINFO**, **PREVIEWDURATION**, **param**, **REPEAT**, **title** |



 

## <a name="remarks"></a>Observaciones

Los cuatro primeros caracteres de una lista de reproducción de metarchivo deben ser "<ASX". Otros elementos definidos dentro del ámbito del elemento **ASX** , como **title** y **Author**, se asocian con la información mostrada por Windows Media Player.

En Windows Media Player, el número de versión de sintaxis es 3,0. Windows Media Player es compatible con todas las versiones anteriores de la sintaxis de metarchivo. Los valores aceptables para el atributo **version** incluyen 3,0 y 3 (sin separador decimal).

Si el valor del atributo **PREVIEWMODE** es Yes, Windows Media Player entra inmediatamente en el modo de vista previa antes de reproducir el primer clip. Cuando Windows Media Player entra en el modo de vista previa, muestra una vista previa de cada clip al que se hace referencia en el metarchivo. El elemento **PREVIEWDURATION** determina la duración de cada vista previa.

El atributo **BANNERBAR** define si Windows Media Player Reserva espacio para un gráfico de banner. Un banner es un gráfico que se muestra en el área de presentación de vídeo mientras se reproduce el contenido multimedia. (Use el elemento **banner** para agregar un banner al contenido). Si el valor de **BANNERBAR** es fijo, Windows Media Player reserva el espacio de banner para cada fragmento de contenido multimedia, tanto si el contenido multimedia tiene un banner. Si una parte del contenido multimedia no tiene un banner asociado, el espacio reservado para uno es negro. Si el valor del atributo **BANNERBAR** es auto, Windows Media Player Reserva espacio para el banner solo cuando el contenido multimedia incluye uno.

Si crea un metarchivo con varios clips (elementos **entry** o **ENTRYREF** ) y establece el valor del atributo **BANNERBAR** en auto, Windows Media Player podría cambiar de tamaño para permitir el espacio para un gráfico de banner para un clip y, a continuación, volver a cambiar el tamaño si el siguiente clip no contiene un gráfico de banner. Si desea que el tamaño de la ventana permanezca igual (excepto cuando cambie el tamaño del vídeo), use el valor fijo del atributo **BANNERBAR** .

El espacio reservado para un gráfico de banner es de 32 píxeles de alto por 194 píxeles de ancho. El espacio reservado aparece debajo de cualquier contenido de vídeo representado y 6 píxeles por encima del borde inferior del área de vídeo, lo que permite espacio para el borde del área de vídeo de 6 píxeles. El espacio reservado del banner está centrado horizontalmente.

Windows Media Player representa el gráfico que comienza en el píxel situado más a la izquierda del espacio de la pancarta. Si el gráfico rellena todo el espacio, aparecerá centrado horizontalmente. De lo contrario, habrá espacio final. Tenga en cuenta que el ancho mínimo de Windows Media Player siempre es mayor que el tamaño del clip de vídeo, independientemente del valor del atributo **BANNERBAR** .

## <a name="examples"></a>Ejemplos


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------|
| Versión<br/> | Windows Media Player versión 70 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





