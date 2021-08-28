---
description: La propiedad CurrentAudioStream establece o recupera el número de la secuencia de audio habilitada.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propiedad CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075975"
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

## <a name="remarks"></a>Comentarios

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Antes de intentar establecer una nueva secuencia de audio, llame a [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para comprobar que la secuencia está disponible.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



