---
title: Atributos de sincronización
description: Los atributos Sync01 a Sync16 son representaciones de cadena de valores de 32 bits que Windows Media Player usa al sincronizar listas de reproducción con uno de hasta 16 dispositivos portátiles.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Atributos de sincronización de Windows Media Player
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718682"
---
# <a name="sync-attributes"></a>Atributos de sincronización

Los atributos **Sync01** a **Sync16** son representaciones de cadena de valores de 32 bits que Windows Media Player usa al sincronizar listas de reproducción con uno de hasta 16 dispositivos portátiles.

## <a name="applies-to"></a>Se aplica a

-   [Reproducción](playlist-attributes-ref.md)

## <a name="remarks"></a>Observaciones

Son atributos de lectura y escritura. Un valor de cero indica que Windows Media Player no debe sincronizar la lista de reproducción con el dispositivo asociado. Un valor mayor que cero indica una prioridad de sincronización para la lista de reproducción determinada.

En función de la entrada del usuario, Windows Media Player establece este atributo para cada una de las listas de reproducción de la biblioteca. Cuando Windows Media Player intenta sincronizar una lista de reproducción con un dispositivo portátil, examina cada lista de reproducción para comparar los valores de los atributos de **Sync**_XX_ que representan la Asociación de dispositivos. Las listas de reproducción con valores inferiores de la **sincronización**_XX_ reciben mayor prioridad de sincronización.

Por ejemplo, la biblioteca puede contener las cuatro listas de reproducción siguientes y los valores de la **sincronización**_XX_ correspondientes:



| Nombre de lista de reproducción | Valor Sync01 |
|---------------|--------------|
| GymMusic. WPL  | 0x0000000D   |
| Relajarse. WPL     | 0x00000020   |
| DriveHome. WPL | 0x00000001   |
| NoGo. WPL      | 0x00000000   |



 

Cuando Windows Media Player sincroniza el dispositivo asociado con el atributo, sincronizará las listas de reproducción en el orden siguiente:

1.  DriveHome. WPL
2.  GymMusic. WPL
3.  Relajarse. WPL

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------|
| Versión<br/> | Windows Media Player 10 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Enumerar listas de reproducción de sincronización**](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





