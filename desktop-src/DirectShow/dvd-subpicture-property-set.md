---
description: Las propiedades de subapicture de DVD controlan el color, el contraste y la salida de la presentación de la subaspección.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propiedades de subpicture de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293e38665fc59cf47b44e6466302655afd2ccf2a909034afd803201f6ea5a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148698"
---
# <a name="dvd-subpicture-property-set"></a>Conjunto de propiedades de subpicture de DVD

Las propiedades de subapicture de DVD controlan el color, el contraste y la salida de la presentación de la subaspección.

En la siguiente información se presentan las constantes y los tipos de datos necesarios que se usarán para este conjunto de propiedades en las llamadas a [**métodos IKsPropertySet.**](ikspropertyset.md) Proporciona valores para los parámetros **GUID** (*guidPropSet*), property ID (*dwPropID*) y property data type (*pPropData*).



| Etiqueta | Value |
|-------------------|----------------------------|
| GUID del conjunto de propiedades | DVDSubPic de AM \_ KSPROPSETID \_ |



 



| Id. de propiedad                           | Descripción                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ DVDSUBPIC \_ COMPOSIT \_ ON | Propiedad de solo establecimiento que habilita o deshabilita la presentación de subaspección. DirectShow define el tipo de datos booleano **\_ AM PROPERTY \_ COMPOSIT \_ ON** para esta propiedad, así como PAM PROPERTY COMPOSIT ON como puntero \_ a este tipo de \_ \_ datos. **TRUE** indica que muestra la subaspección, **FALSE** indica deshabilitarla. Consulte la parte WDM de Windows DDK para obtener más información. |
| PROPIEDAD \_ AM \_ DVDSUBPIC \_ HLI          | Propiedad de solo establecimiento que especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiarán. El tipo de datos [**es AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) Vea la sección Comentarios.                                                                                                                                                                                |
| PALETA \_ \_ DVDSUBPIC DE LA \_ PROPIEDAD AM      | Establece la paleta para una subaspección. El tipo de datos [**es AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentarios

La **propiedad \_ \_ DVDSUBPIC \_ HLI** de AM PROPERTY es de solo establecimiento. Especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiarán. Esto difiere de la especificación de DVD-Video, en que el navegador de DVD de Microsoft analiza toda la información de botón y teclado y pasa solo un rectángulo de resaltado al descodificador de subpicture en un momento dado. Como resultado, la información de resaltado se envía al descodificador con más frecuencia de la que está presente en la secuencia de DVD.

La información de resaltado llega de forma asincrónica al flujo de datos. El descodificador usa las marcas de tiempo de inicio y finalización resaltadas para correlacionar la información de resaltado con la información de subaspección pertinente, si existe. Si el descodificador no ha recibido ninguna información de secuencia de subaspección para las marcas de tiempo solicitadas, el descodificador asume que la información de resaltado es independiente y no se aplica a una subaspección. En este caso, el descodificador asume que la información de color y contraste es del mismo color.

Los datos no están completamente en formato de disco DVD. Microsoft proporciona una estructura adicional de tipo [**AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) que se pasa como parámetro a esta propiedad. Esta estructura describe el botón seleccionado actualmente en la información de resaltado de DVD.

El navegador de DVD procesa toda la información de pulsación de tecla y envía nueva información de resaltado cada vez que cambia el estado de un botón. La información describe solo un modo de un botón a la vez. Incluye un rectángulo de presentación en coordenadas de píxeles de la pantalla o una presentación de la subaspección, si está presente. La estructura también contiene información de color y contraste, pero solo para el estado actual del botón seleccionado actualmente. El formato se define en la especificación de DVD.

La información de resaltado contiene marcas de tiempo de inicio y finalización. Se encuentran en las mismas unidades que otras marcas de tiempo, con dos excepciones: una marca de tiempo de inicio de 0xFFFFFFFF significa que la propiedad de resaltado es efectiva tras la recepción y una marca de tiempo de finalización de 0xFFFFFFFF significa que la propiedad de resaltado es válida hasta que se recibe el resaltado siguiente.

El campo HLISS se define en la especificación de DVD. Un valor de cero indica que todos los resaltados no son válidos y el descodificador debe deshabilitar todos los resaltados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




