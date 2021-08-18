---
description: El atributo previewmode especifica el modo de vista previa del grupo. Si el valor es TRUE, los fotogramas se pueden descartar durante la versión preliminar. De lo contrario, no se descarta ningún fotograma durante la versión preliminar. El valor predeterminado es TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: atributo previewmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baed13417539432a3a2958b96b214c3c63ae12f2802586ca220669b1497d91f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748275"
---
# <a name="previewmode-attribute"></a>atributo previewmode

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `previewmode` atributo especifica el modo de vista previa del grupo. Si el valor es **TRUE,** los fotogramas se podrían descartar durante la versión preliminar. De lo contrario, no se descarta ningún fotograma durante la versión preliminar. El valor predeterminado es **TRUE.**

## <a name="possible-values"></a>Valores posibles

Los valores siguientes se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**Grupo**](group-element.md)

## <a name="remarks"></a>Comentarios

En la configuración predeterminada, los fotogramas se descartan al obtener una vista previa de los efectos o transiciones lentos, para mantener el vídeo sincronizado con el audio. Como resultado, el vídeo podría parecer descortesado. Al establecer este atributo en **FALSE,** se fuerza la representación de cada fotograma durante la versión preliminar, lo que posiblemente provocará que el vídeo se des sincronice con el audio. Los fotogramas nunca se descartan al escribir en un archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



