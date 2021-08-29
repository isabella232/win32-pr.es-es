---
title: Método ClosedCaption.getSAMIStyleName
description: El método getSAMIStyleName recupera el nombre de un estilo admitido por el archivo SAMI actual.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- Método getSAMIStyleName Reproductor de Windows Media
- Método getSAMIStyleName Reproductor de Windows Media , clase ClosedCaption
- Clase ClosedCaption Reproductor de Windows Media método , getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7b7a8a23c47a464e1b192a4a652d87043765260a1016c707fa8d6c85c22b575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135808"
---
# <a name="closedcaptiongetsamistylename-method"></a>Método ClosedCaption.getSAMIStyleName

El **método getSAMIStyleName** recupera el nombre de un estilo admitido por el archivo SAMI actual.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*index* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica el índice del nombre de estilo que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que contiene el nombre del estilo tal como se especifica en el archivo SAMI.

## <a name="remarks"></a>Comentarios

Los estilos de un archivo SAMI se indexa en el orden que se muestra en el archivo, empezando por cero.

Este método no se puede usar hasta que se abra un archivo multimedia digital *(Reproductor de*.**openState** es igual a 13).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption (objeto)**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





