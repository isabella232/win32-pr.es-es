---
description: El atributo previewmode especifica el modo de vista previa para el grupo. Si el valor es TRUE, los fotogramas podrían quitarse durante la vista previa. De lo contrario, no se quita ningún fotograma durante la vista previa. El valor predeterminado es TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Atributo previewmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422888"
---
# <a name="previewmode-attribute"></a>Atributo previewmode

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `previewmode` atributo especifica el modo de vista previa para el grupo. Si el valor es **true**, los fotogramas podrían quitarse durante la vista previa. De lo contrario, no se quita ningún fotograma durante la vista previa. El valor predeterminado es **true**.

## <a name="possible-values"></a>Valores posibles

Los siguientes valores se definen como TRUE: y, Y, t, T, 1. Los valores siguientes se definen como FALSE: n, N, f, F, 0 (cero).

## <a name="applies-to"></a>Se aplica a

[**agrupamiento**](group-element.md)

## <a name="remarks"></a>Observaciones

En la configuración predeterminada, se quitan los fotogramas mientras se realiza una vista previa de los efectos o las transiciones lentas para mantener el vídeo sincronizado con el audio. Es posible que el vídeo parezca entrecortado como resultado. Si se establece este atributo en **false** , cada fotograma se representará durante la versión preliminar, lo que podría dar lugar a que el vídeo deje de estar sincronizado con el audio. Los fotogramas nunca se quitan cuando se escribe en un archivo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



