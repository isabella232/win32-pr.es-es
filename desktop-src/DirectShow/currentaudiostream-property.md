---
description: La propiedad CurrentAudioStream establece o recupera el número de la secuencia de audio habilitada.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propiedad CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659273"
---
# <a name="currentaudiostream-property"></a>Propiedad CurrentAudioStream

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentAudioStream` propiedad establece o recupera el número de la secuencia de audio habilitada.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero comprendido entre 0 y 7 que indica la secuencia de audio actual.

## <a name="remarks"></a>Observaciones

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Antes de intentar establecer una nueva secuencia de audio, llame a [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para comprobar que la secuencia está disponible.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



