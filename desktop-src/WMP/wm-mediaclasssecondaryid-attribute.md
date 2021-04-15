---
title: Atributo WM/MediaClassSecondaryID
description: El atributo WM/MediaClassSecondaryID es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- Media Player de Windows de atributos de WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708712"
---
# <a name="wmmediaclasssecondaryid-attribute"></a>Atributo WM/MediaClassSecondaryID

El atributo **WM/MediaClassSecondaryID** es un GUID que especifica la clase multimedia secundaria, que es una subclase de la clase multimedia principal.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Otros elementos](other-item-attributes.md)
-   [Elementos de fotografía](photo-item-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

En la tabla siguiente se enumeran los GUID admitidos y sus descripciones.



| GUID                                 | Descripción                                    |
|--------------------------------------|------------------------------------------------|
| D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC | El objeto multimedia representa una lista de reproducción estática. |
| EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D | El objeto multimedia representa una lista de reproducción automática.  |



 

**MediaClassSecondaryID** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMMediaClassSecondaryID.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | El elemento de foto solo se admite en Windows Media Player 10 o posterior. el elemento de radio solo se admite en Windows Media Player 9 series todos los demás elementos se admiten en Windows Media Player series 9 y versiones posteriores<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





