---
title: Atributo WM/WMCollectionGroupID
description: El atributo WM/WMCollectionGroupID es un GUID que identifica el grupo que contiene la colección a la que pertenece el elemento.
ms.assetid: 5383fb12-fc16-474e-b9a0-c1e69b86a057
keywords:
- Media Player de Windows de atributos de WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681ad7049520ed77de3ebb385e74efcfef66b4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718856"
---
# <a name="wmwmcollectiongroupid-attribute"></a>Atributo WM/WMCollectionGroupID

El atributo **WM/WMCollectionGroupID** es un GUID que identifica el grupo que contiene la colección a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**WMCollectionGroupID** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMCollectionGroupID.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





