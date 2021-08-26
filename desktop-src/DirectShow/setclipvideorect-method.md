---
description: El método SetClipVideoRect acerca la presentación del vídeo a la subrectangle especificada.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Método SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7741a2604ed1c2896b105295020893e23b447e3fa6f6ab7c53def92aa508c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078875"
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

## <a name="remarks"></a>Comentarios

Cuando se establece un nuevo rectángulo de recorte, el objeto amplía ese área para ajustarse a las dimensiones de presentación generales de la aplicación. Esto crea el efecto de acercar en un área determinada de la pantalla. Para especificar el rectángulo, cree un nuevo [objeto DVDRect](dvdrect-object.md) y rellene sus propiedades.

El rectángulo más común para la presentación de vídeo es 720 x 540.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



