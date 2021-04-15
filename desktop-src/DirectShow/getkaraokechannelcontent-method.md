---
description: El método GetKaraokeChannelContent recupera un valor que indica el tipo de contenido del canal de karaoke especificado en la secuencia especificada.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Método GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677121"
---
# <a name="getkaraokechannelcontent-method"></a>Método GetKaraokeChannelContent

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetKaraokeChannelContent` método recupera un valor que indica el tipo de contenido del canal de karaoke especificado en la secuencia especificada.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica la secuencia de audio como un entero.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

Especifica el canal como un entero. Los valores posibles para cada canal son:



| Value  | Descripción    |
|--------|----------------|
| 0x0001 | Guía de vocal 1  |
| 0x0002 | Guía vocal 2  |
| 0x0004 | Guía Melody 1 |
| 0x0008 | Guía Melody 2 |
| 0x0010 | Guía Melody A |
| 0x0020 | Guía Melody B |
| 0x0040 | Efecto de sonido A |
| 0x0080 | Efecto de sonido B |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero cuyos bits individuales especifican el contenido del canal de karaoke.

## <a name="remarks"></a>Observaciones

La numeración de canales de audio de DVD se basa en cero, por lo que los canales 2, 3 y 4 son los canales de karaoke auxiliares. Después de que el método vuelva, realice una operación and bit a bit en *iContent* para determinar el contenido de cada canal. Dado que un único canal puede tener más de un tipo de contenido registrado, debe comprobar todos los valores posibles incluso después de encontrar una coincidencia.

Una vez que el usuario conoce el contenido de cada canal, debe ser capaz de ajustar el volumen o activar o desactivar los canales individuales según sea necesario. Implemente esta funcionalidad en la aplicación mediante la propiedad [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .

> [!Note]  
> Para reproducir discos Karaoke, el descodificador de audio en el sistema del usuario debe ser compatible con la implementación de Karaoke de DirectShow 8.

 

 

 



