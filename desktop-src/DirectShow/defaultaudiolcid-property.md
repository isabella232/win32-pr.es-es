---
description: La propiedad DVDAdm. DefaultAudioLCID establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propiedad DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677175"
---
# <a name="defaultaudiolcid-property"></a>Propiedad DefaultAudioLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `DVDAdm.DefaultAudioLCID` propiedad establece o recupera la configuración del registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el LCID de audio predeterminado especificado por el usuario, tal como se almacena en la configuración del registro de la aplicación de DVD. Este valor no es necesariamente el mismo que el flujo de audio predeterminado que se creó en el DVD.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Si no se especifica ningún LCID de audio predeterminado, el objeto MSDVDAdm reproducirá la secuencia de audio marcada como la secuencia predeterminada en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



