---
description: El método GetKaraokeChannelContent recupera un valor que indica el tipo de contenido en el canal de canal de canal especificado en la secuencia especificada.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: GetKaraokeChannelContent (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0353ebda6469627b5f41209b780fc1403c51940705be72d6acaa139d8320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812495"
---
# <a name="getkaraokechannelcontent-method"></a>GetKaraokeChannelContent (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método recupera un valor que indica el tipo de contenido en el canal de Canal de Canal especificado `GetKaraokeChannelContent` en la secuencia especificada.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica la secuencia de audio como un entero.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

Especifica el canal como entero. Los valores posibles para cada canal son:



| Valor  | Descripción    |
|--------|----------------|
| 0x0001 | Guide Voz 1  |
| 0x0002 | Guide Voz 2  |
| 0x0004 | Guía 1 |
| 0x0008 | Guía 2 |
| 0x0010 | Guía A |
| 0x0020 | Guía B |
| 0x0040 | Efecto de sonido A |
| 0x0080 | Efecto de sonido B |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero cuyos bits individuales especifican el contenido del canal de canal de Canal.

## <a name="remarks"></a>Comentarios

La numeración de canales de audio de DVD es de base cero, por lo que los canales 2, 3 y 4 son los canales auxiliares de canal. Una vez que el método vuelva, realice una operación AND bit a bit *en iContent* para determinar el contenido de cada canal. Dado que un único canal puede tener más de un tipo de contenido registrado en él, debe probar todos los valores posibles incluso después de encontrar una coincidencia.

Una vez que el usuario conoce el contenido de cada canal, debe poder ajustar el volumen o activar o desactivar los canales individuales según sea necesario. Implemente esta funcionalidad en la aplicación mediante la [**propiedadAudioPresentationMode.**](karaokeaudiopresentationmode-property.md)

> [!Note]  
> Para reproducir discos de sonido, el descodificador de audio del sistema del usuario debe ser compatible con la implementación de DirectShow 8.

 

 

 



