---
description: Cuando el filtro del navegador de DVD entra en el modo de karaoke, informa al descodificador de audio a través de la \_ propiedad AM \_ DVDKARAOKE \_ enable.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propiedades de Karaoke de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679176"
---
# <a name="dvd-karaoke-property-set"></a>Conjunto de propiedades de Karaoke de DVD

Cuando el filtro del [navegador de DVD](dvd-navigator-filter.md) entra en el modo de karaoke, informa al descodificador de audio a través de la **\_ propiedad AM \_ DVDKARAOKE \_ enable** . A continuación, el descodificador debe silenciar los canales de audio del 2 al 5 hasta que reciba desde el navegador de DVD una propiedad de **\_ \_ \_ datos DVDKARAOKE de la propiedad AM** con un puntero a una estructura de datos [**AM \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) que indique cómo se van a mezclar los canales auxiliares.



|                   |                             |
|-------------------|-----------------------------|
| GUID del conjunto de propiedades | \_DvdKaraoke KSPROPSETID \_ AM |



 



| Id. de propiedad                      | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_propiedad AM \_ DVDKARAOKE \_ enable | Valor BOOLEANO. El navegador de DVD envía al descodificador una \_ propiedad AM \_ DVDKARAOKE \_ enable con un valor de **true** para habilitar Karaoke downmixing o **false** para deshabilitarlo.                                                                                                                                    |
| \_ \_ datos DVDKARAOKE de la propiedad AM \_   | El navegador de DVD envía al descodificador una \_ \_ propiedad de \_ datos DVDKARAOKE de la propiedad AM con un puntero a una estructura [**AM \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) para cambiar la configuración de downmix; es decir, para activar o desactivar determinados canales de karaoke y dirigirlos al canal de salida derecho o izquierdo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




