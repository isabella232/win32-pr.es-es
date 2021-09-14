---
title: Evento Player.CurrentMediaItemAvailable
description: El evento CurrentMediaItemAvailable tiene lugar cuando está disponible un elemento de metadatos gráfico en el elemento multimedia actual. | Evento Player.CurrentMediaItemAvailable
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Evento CurrentMediaItemAvailable Reproductor de Windows Media
- Evento CurrentMediaItemAvailable Reproductor de Windows Media , clase Player
- Clase player Reproductor de Windows Media evento , CurrentMediaItemAvailable
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070998"
---
# <a name="playercurrentmediaitemavailable-event"></a>Evento Player.CurrentMediaItemAvailable

El **evento CurrentMediaItemAvailable** tiene lugar cuando está disponible un elemento de metadatos gráfico en el elemento multimedia actual.

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

Dado que la reproducción puede comenzar antes de que un elemento multimedia se descargue por completo, es posible que los gráficos de metadatos contenidos en el elemento multimedia (por ejemplo, la portada del álbum) no estén disponibles cuando empiece a reproducirse. Este evento le avisa cuando finaliza la descarga de un elemento gráfico de metadatos. A continuación, puede recuperar **el objeto Media** pasando el valor de *bstrItemName* a *MediaCollection*. **Método getByName,** después del cual puede acceder al elemento gráfico de metadatos mediante *Media*. **getItemInfoByType y** especifica **WM/Picture** para el nombre del atributo.

El valor de los parámetros de evento se especifica mediante Reproductor de Windows Media y se puede acceder a un método o pasarlo a un método en un archivo JScript importado con el nombre de parámetro especificado. Este nombre de parámetro debe escribirse exactamente como se muestra, incluida la mayúscula.

**Reproductor de Windows Media 10 Mobile:** Este evento no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**MediaCollection.getByName**](mediacollection-getbyname.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> </dl>

 

 





