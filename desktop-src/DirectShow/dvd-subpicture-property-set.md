---
description: Las propiedades de subimagen de DVD controlan el color, el contraste y la salida de la pantalla de la imagen.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propiedades de subimagen de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680444"
---
# <a name="dvd-subpicture-property-set"></a>Conjunto de propiedades de subimagen de DVD

Las propiedades de subimagen de DVD controlan el color, el contraste y la salida de la pantalla de la imagen.

La siguiente información presenta las constantes y los tipos de datos necesarios para usar en esta propiedad establecida en llamadas a métodos [**IKsPropertySet**](ikspropertyset.md) . Proporciona valores para los parámetros **GUID** (*GUIDPROPSET*), ID. de propiedad (*dwPropID*) y tipo de datos de propiedad (*pPropData*).



|                   |                            |
|-------------------|----------------------------|
| GUID del conjunto de propiedades | \_DvdSubPic KSPROPSETID \_ AM |



 



| Id. de propiedad                           | Descripción                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_propiedad AM \_ DVDSUBPIC \_ \_ | Propiedad de solo establecimiento que habilita o deshabilita la presentación de la subimagen. DirectShow define la **\_ propiedad \_ de AM composiciones \_ en** el tipo de datos booleano para esta propiedad, así como la propiedad de PAM componer \_ \_ \_ en como un puntero a este tipo de datos. **True** indica que se muestra la subimagen, **false** indica deshabilitarla. Para obtener más información, consulte la parte WDM del DDK de Windows. |
| \_propiedad AM \_ DVDSUBPIC \_ HLI          | Propiedad de solo establecimiento que especifica un rectángulo de subimagen o pantalla cuyo color o contraste se van a cambiar. El tipo de datos es la [**\_ propiedad AM \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli). Vea la sección Comentarios.                                                                                                                                                                                |
| \_propiedad AM \_ DVDSUBPIC \_ paleta      | Establece la paleta para una subimagen. El tipo de datos es la [**\_ propiedad AM \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Observaciones

La propiedad AM de la propiedad **\_ \_ DVDSUBPIC \_ HLI** es de solo configuración. Especifica un rectángulo de subimagen o pantalla cuyo color o contraste se cambiará. Esto difiere de la especificación de DVD-Video, en que el navegador de DVD de Microsoft analiza toda la información del botón y del teclado, y pasa solo un rectángulo de resaltado al descodificador de la subimagen en un momento dado. Como resultado, la información de resaltado se envía al descodificador con más frecuencia de la que se encuentra en la secuencia de DVD.

La información de resaltado llega asincrónicamente al flujo de datos. El descodificador utiliza las marcas de tiempo de inicio y finalización de resaltado para correlacionar la información de resaltado con la información de la subimagen correspondiente, si existe. Si el descodificador no ha recibido ninguna información de flujo de subimagen para las marcas de tiempo solicitadas, el descodificador supone que la información de resaltado es independiente y no se aplica a una subimagen. En este caso, el descodificador supone que la información de color y contraste es todo el mismo color.

Los datos no tienen un formato de disco completo en DVD. Microsoft proporciona una estructura adicional de la [**\_ propiedad \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) de tipo AM que se pasa como parámetro a esta propiedad. Esta estructura describe el botón seleccionado actualmente de la información de resaltado del DVD.

El navegador de DVD procesa toda la información sobre las pulsaciones de teclas y envía información de resaltado nueva cada vez que cambia el estado de un botón. La información describe solo un modo de un botón a la vez. Incluye un rectángulo de presentación en coordenadas en píxeles de la pantalla, o una presentación de la subimagen, si está presente. La estructura también contiene información sobre el color y el contraste, pero solo para el estado actual del botón seleccionado actualmente. El formato se define en la especificación de DVD.

La información de resaltado contiene marcas de tiempo de inicio y finalización. Se encuentran en las mismas unidades que otras marcas de tiempo, con dos excepciones: una marca de hora de inicio de 0xFFFFFFFF significa que la propiedad resaltada es efectiva en la recepción y una marca de hora de finalización de 0xFFFFFFFF significa que la propiedad resaltado es válida hasta que se recibe el siguiente resaltado.

El campo HLISS es como se define en la especificación de DVD. Un valor de cero indica que todos los resaltados no son válidos y el descodificador debe deshabilitar todos los resaltados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




