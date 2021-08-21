---
description: Cuando el filtro DVD Navigator entra en modo de vídeo, informa al descodificador de audio a través de la propiedad \_ \_ DVDKARAOKE ENABLE de AM \_ PROPERTY.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propiedades DVD Dvd Dvd Dvdmedia.h
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f3f7674b240934ae7440858b7317fd1abaf9b7833e36f80d7edc6cc185bc932
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016023"
---
# <a name="dvd-karaoke-property-set"></a>Conjunto de propiedades DVD Dvd Dvd

Cuando el [filtro DVD Navigator](dvd-navigator-filter.md) entra en modo de vídeo, informa al descodificador de audio a través de la propiedad **\_ \_ DVDKARAOKE \_ ENABLE de AM PROPERTY.** A continuación, el descodificador debe silenciar los canales de audio del 2 al 5 hasta que reciba desde el navegador de DVD una propiedad **\_ \_ DVDKARAOKE \_ DATA** de AM PROPERTY con un puntero a una estructura de datos [**\_ DVDKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM que indica cómo se van a mezclar los canales auxiliares.



| Etiqueta | Valor |
|-------------------|-----------------------------|
| GUID del conjunto de propiedades | DVDKaraoke de AM \_ KSPROPSETID \_ |



 



| Id. de propiedad                      | Descripción                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HABILITACIÓN \_ DE \_ DVDKARAOKE DE LA \_ PROPIEDAD AM | Valor booleano. El navegador de DVD envía al descodificador una PROPIEDAD DE AM DVDKARAOKE ENABLE con un valor de TRUE para habilitar la mezclación de bajada o \_ \_ FALSE para \_ deshabilitarlo.                                                                                                                                      |
| DATOS \_ \_ DVDKARAOKE DE LA PROPIEDAD \_ AM   | El navegador de DVD envía al descodificador una propiedad DVDKARAOKE DATA de AM PROPERTY con un puntero a una estructura \_ \_ \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM para cambiar la configuración de la mezcla inferior; es decir, para activar o desactivar determinados canales de canal de canal y dirigirlos al canal de salida derecho o izquierdo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 




