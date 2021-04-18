---
title: Reproductor. estado
description: La propiedad status recupera un valor que indica el estado de Windows Media Player.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Windows Media Player de Player. status
topic_type:
- apiref
api_name:
- Player.status
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d54c71e6ab8ece61fb97960bd2956393b1ae584
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708245"
---
# <a name="playerstatus"></a>Reproductor. estado

La propiedad **status** recupera un valor que indica el estado de Windows Media Player.

## <a name="syntax"></a>Sintaxis

*reproductor* . **Estado** de

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo lectura.

## <a name="remarks"></a>Observaciones

Los valores contenidos en esta propiedad están sujetos a cambios en cualquier momento y deben usarse solo con fines de presentación.

El evento **StatusChange** se desencadena cuando esta propiedad cambia el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 7,0 o posterior.<br/>                                      |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player. StatusChange**](player-player-statuschange.md)
</dt> </dl>

 

 





