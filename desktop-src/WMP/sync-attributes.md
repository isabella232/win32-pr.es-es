---
title: Atributos de sincronización
description: Los atributos Sync01 a Sync16 son representaciones de cadena de valores de 32 bits que Reproductor de Windows Media usa cuando sincroniza listas de reproducción con uno de hasta 16 dispositivos portátiles.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Sincronización de atributos Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e720598b17db6b073524d80afc8f39dd6e6f87e777246b5bdb60294b161fa1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134758"
---
# <a name="sync-attributes"></a>Atributos de sincronización

Los atributos **Sync01** a **Sync16** son representaciones de cadena de valores de 32 bits que Reproductor de Windows Media usa cuando sincroniza listas de reproducción con uno de hasta 16 dispositivos portátiles.

## <a name="applies-to"></a>Se aplica a

-   [Listas](playlist-attributes-ref.md)

## <a name="remarks"></a>Comentarios

Estos son atributos de lectura y escritura. Un valor de cero indica que Reproductor de Windows Media no debe sincronizar la lista de reproducción con el dispositivo asociado. Un valor mayor que cero indica una prioridad de sincronización para la lista de reproducción determinada.

En función de la entrada del usuario, Reproductor de Windows Media este atributo para cada una de las listas de reproducción de la biblioteca. Cuando Reproductor de Windows Media sincronizar una lista de reproducción con un dispositivo portátil, examina cada lista de reproducción para comparar los valores de los atributos **sync**_XX_ que representan la asociación del dispositivo. Las listas de reproducción con valores **xx de sincronización**_inferiores_ reciben una prioridad de sincronización mayor.

Por ejemplo, la biblioteca puede contener las cuatro listas de reproducción siguientes y los **respectivos valores de Sync**_XX:_



| Nombre de la lista de reproducción | Valor Sync01 |
|---------------|--------------|
| Descontrol.WPL  | 0x0000000D   |
| Relax.WPL     | 0x00000020   |
| DriveHome.WPL | 0x00000001   |
| NoGo.WPL      | 0x00000000   |



 

Cuando Reproductor de Windows Media el dispositivo asociado al atributo , sincronizará las listas de reproducción en el orden siguiente:

1.  DriveHome.WPL
2.  Descontrol.WPL
3.  Relax.WPL

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Enumeración de listas de reproducción de sincronización**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





