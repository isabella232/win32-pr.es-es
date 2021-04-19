---
title: ClosedCaption. getSAMIStyleName, método
description: El método getSAMIStyleName recupera el nombre de un estilo compatible con el archivo SAMI actual.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- método getSAMIStyleName de Windows Media Player
- método getSAMIStyleName de Windows Media Player, clase ClosedCaption
- Clase ClosedCaption Windows Media Player, método getSAMIStyleName
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
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699540"
---
# <a name="closedcaptiongetsamistylename-method"></a>ClosedCaption. getSAMIStyleName, método

El método **getSAMIStyleName** recupera el nombre de un estilo compatible con el archivo Sami actual.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del nombre de estilo que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena** que contiene el nombre del estilo tal y como se especifica en el archivo Sami.

## <a name="remarks"></a>Observaciones

Los estilos de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.

Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**ClosedCaption.SAMIStyle**](closedcaption-samistyle.md)
</dt> </dl>

 

 





