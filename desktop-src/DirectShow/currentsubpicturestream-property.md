---
description: La propiedad CurrentSubpictureStream establece o recupera la secuencia de subimagen actual.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Propiedad CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538079"
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

## <a name="remarks"></a>Observaciones

Los valores posibles de esta propiedad son:



| Value   | Descripción              |
|---------|--------------------------|
| de 0 a 31 | Secuencia de subimagen    |
| 63      | Secuencia de velocidad de bits baja silenciada |



 

Esta propiedad es de lectura/escritura y no tiene ningún valor predeterminado. Antes de establecer una nueva secuencia de subimagen, llame a [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) para comprobar que la secuencia está disponible.

Al establecer esta propiedad, la propiedad [**subpictureon**](subpictureon-property.md) se cambia a **true**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Subimagen en**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



