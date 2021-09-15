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
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466396"
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

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

En la tabla siguiente se enumeran los GUID admitidos y sus descripciones.



| GUID                                 | Descripción                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | El objeto multimedia representa una lista de reproducción estática. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | El objeto multimedia representa una lista de reproducción automática.  |



 

**MediaClassSecondaryID** es un alias para este atributo.

La Windows DEL SDK de formato multimedia para este atributo es g \_ wszWMMediaClassSecondaryID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | El elemento de foto solo se admite en Reproductor de Windows Media 10 o posterior. El elemento de radio solo se admite en la serie Reproductor de Windows Media 9. Todos los demás elementos se admiten en Reproductor de Windows Media serie 9 y versiones posteriores<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





