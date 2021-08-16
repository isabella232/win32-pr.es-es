---
description: La propiedad CurrentSubpictureStream establece o recupera la secuencia de subimagen actual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propiedad CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821959"
---
# <a name="currentsubpicturestream-property"></a>Propiedad CurrentSubpictureStream

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentSubpictureStream` propiedad establece o recupera la secuencia de subimagen actual.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa la secuencia.

## <a name="remarks"></a>Comentarios

Los valores posibles de esta propiedad son:



| Valor   | Descripción              |
|---------|--------------------------|
| De 0 a 31 | Secuencia de subimagen    |
| 63      | Secuencia de velocidad de bits baja muted |



 

Esta propiedad es de lectura y escritura sin ningún valor predeterminado. Antes de establecer una nueva secuencia de subpicture, llame a [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para comprobar que la secuencia está disponible.

Establecer esta propiedad hace que [**la propiedad SubpictureOn**](subpictureon-property.md) cambie a **True.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



