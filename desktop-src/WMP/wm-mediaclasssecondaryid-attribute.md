---
title: Atributo WM/MediaClassSecondaryID
description: El atributo WM/MediaClassSecondaryID es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Atributo WM/MediaClassSecondaryID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9582fc3db713b8db945ec17534f1dc9c951402eea88489285526d6a3cfbdf147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000995"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Atributo WM/MediaClassSecondaryID

El **atributo WM/MediaClassSecondaryID** es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotos](photo-item-attributes.md)
-   [Listas](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

En la tabla siguiente se enumeran los GUID admitidos y sus descripciones.



| GUID                                 | Descripción                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | El objeto multimedia representa una lista de reproducción estática. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | El objeto multimedia representa una lista de reproducción automática.  |



 

**MediaClassSecondaryID** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMMediaClassSecondaryID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | El elemento de foto solo se admite en Reproductor de Windows Media 10 o posterior. El elemento de radio solo se admite en la serie 9 de Reproductor de Windows Media Todos los demás elementos se admiten en Reproductor de Windows Media serie 9 y versiones posteriores<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





