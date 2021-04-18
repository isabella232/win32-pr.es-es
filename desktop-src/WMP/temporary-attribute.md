---
title: Atributo temporal
description: El atributo Temporary especifica si una lista de reproducción es temporal.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Media Player de atributos temporales de Windows
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718679"
---
# <a name="temporary-attribute"></a>Atributo temporal

El atributo **Temporary** especifica si una lista de reproducción es temporal.

**Comentarios:**

Si recuperó una lista de reproducción de la biblioteca, los cambios que realice en la lista de reproducción se reflejarán en la biblioteca del usuario. Para evitar esto, llame a [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) pasando el nombre de atributo "Temporary" y el valor "true". Esto convierte la instancia de la lista de reproducción en una lista de reproducción temporal, que es segura de editar sin cambiar la lista de reproducción original.

**Se aplica a**

-   [Reproducción](playlist-attributes-ref.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------|
| Versión<br/> | Reproductor de Windows Media 11<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





