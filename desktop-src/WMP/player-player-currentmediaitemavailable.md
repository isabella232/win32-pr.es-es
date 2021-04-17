---
title: Evento Player. CurrentMediaItemAvailable
description: El evento CurrentMediaItemAvailable se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible. | Evento Player. CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Media Player CurrentMediaItemAvailable de eventos de Windows
- Evento CurrentMediaItemAvailable de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento CurrentMediaItemAvailable
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708677"
---
# <a name="playercurrentmediaitemavailable-event"></a>Evento Player. CurrentMediaItemAvailable

El evento **CurrentMediaItemAvailable** se produce cuando un elemento de metadatos gráfico del elemento multimedia actual está disponible.

## <a name="syntax"></a>Sintaxis


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Cadena** que contiene el nombre del elemento multimedia actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Dado que la reproducción puede comenzar antes de que un elemento multimedia se descargue por completo, es posible que los gráficos de metadatos contenidos en el elemento multimedia (por ejemplo, la portada del álbum) no estén disponibles cuando comience a reproducirse. Este evento le avisa cuando termina la descarga de un elemento de gráfico de metadatos. A continuación, puede recuperar el objeto **multimedia** pasando el valor de *bstrItemName* a *MediaCollection*. método **getByName** , después del cual se puede tener acceso al elemento gráfico de metadatos mediante el uso de *medios*. **getItemInfoByType** y especificando **WM/imagen** para el nombre del atributo.

El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo JScript importado mediante el nombre de parámetro dado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.

**Windows Media Player 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection.getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





