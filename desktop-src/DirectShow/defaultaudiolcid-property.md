---
description: La propiedad DVDAdm.DefaultAudioLCID establece o recupera la configuración del Registro para el LCID predeterminado especificado por el usuario para la secuencia de audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propiedad DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7ebcd864f8ac3bff8cfd8556703dd091985a72c0dfea4f0eefb9f974213165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953014"
---
# <a name="defaultaudiolcid-property"></a>Propiedad DefaultAudioLCID

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La propiedad establece o recupera la configuración del Registro para el LCID predeterminado especificado por el `DVDAdm.DefaultAudioLCID` usuario para la secuencia de audio.

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor Entero que representa el LCID de audio predeterminado especificado por el usuario tal como se almacena en la configuración del Registro para la aplicación de DVD. Este valor no es necesariamente el mismo que el flujo de audio predeterminado que se ha escrito en el DVD.

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Si no se especifica ningún LCID de audio predeterminado, el objeto MSDVDAdm reproducirá la secuencia de audio marcada como la secuencia predeterminada en el disco.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Objeto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



