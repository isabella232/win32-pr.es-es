---
description: Cuando el filtro navegador de DVD entra en modo de vídeo, informa al descodificador de audio a través de la propiedad \_ \_ DVDKARAOKE ENABLE de AM \_ PROPERTY.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propiedades DVD Dvd Dvd Dvdmedia.h
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909073"
---
# <a name="dvd-karaoke-property-set"></a>Conjunto de propiedades DVD Dvd Dvd

Cuando el [filtro navegador de DVD](dvd-navigator-filter.md) entra en modo de vídeo, informa al descodificador de audio a través de la propiedad **\_ \_ DVDKARAOKE \_ ENABLE de AM PROPERTY.** A continuación, el descodificador debe silenciar los canales de audio del 2 al 5 hasta que reciba desde el navegador de DVD una propiedad DE AM **\_ PROPERTY \_ DVDKARAOKE \_ DATA** con un puntero a una estructura de datos [**\_ DVDKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM que indica cómo se van a mezclar los canales auxiliares.



| Etiqueta | Value |
|-------------------|-----------------------------|
| GUID del conjunto de propiedades | DVDKaraoke de AM \_ KSPROPSETID \_ |



 



| Id. de propiedad                      | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HABILITACIÓN \_ \_ DE DVDKARAOKE DE LA PROPIEDAD \_ AM | Valor booleano. El navegador de DVD envía al descodificador una PROPIEDAD DE AM DVDKARAOKE ENABLE con un valor de TRUE para habilitar la remezclación de alias o \_ \_ FALSE para \_ deshabilitarla.                                                                                                                                      |
| DATOS \_ \_ DVDKARAOKE DE LA PROPIEDAD \_ AM   | El navegador de DVD envía al descodificador una propiedad DVDKARAOKE DATA de AM PROPERTY con un puntero a una estructura \_ \_ \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM para cambiar la configuración de la mezcla inferior; es decir, para activar o desactivar determinados canales y dirigirlos al canal de salida derecho o izquierdo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




