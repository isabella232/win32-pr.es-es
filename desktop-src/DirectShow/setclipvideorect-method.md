---
description: El método SetClipVideoRect acerca la presentación del vídeo a la subrectangle especificada.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061610"
---
# <a name="setclipvideorect-method"></a>Método SetClipVideoRect

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetClipVideoRect` método acerca la presentación del vídeo a la subrectangle especificada.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Especifica un objeto [DVDRect,](dvdrect-object.md) que contiene el rectángulo de recorte.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se establece un nuevo rectángulo de recorte, el objeto amplía esa área para ajustarse a las dimensiones de presentación generales de la aplicación. Esto crea el efecto de acercar en un área determinada de la pantalla. Para especificar el rectángulo, cree un nuevo [objeto DVDRect](dvdrect-object.md) y rellene sus propiedades.

El rectángulo más común para la presentación de vídeo es 720 x 540.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



