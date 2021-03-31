---
description: El método SetClipVideoRect amplía la presentación de vídeo al subrectángulo especificado.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805870"
---
# <a name="setclipvideorect-method"></a>Método SetClipVideoRect

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SetClipVideoRect` método amplía la presentación del vídeo al subrectángulo especificado.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Especifica un objeto [DVDRect](dvdrect-object.md) , que contiene el rectángulo de recorte.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se establece un nuevo rectángulo de recorte, el objeto amplía ese área para ajustarse a las dimensiones generales de presentación de la aplicación. Esto crea el efecto acercar en un área determinada de la pantalla. Para especificar el rectángulo, cree un nuevo objeto [DVDRect](dvdrect-object.md) y rellene sus propiedades.

El rectángulo más común para la visualización de vídeo es 720 x 540.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



