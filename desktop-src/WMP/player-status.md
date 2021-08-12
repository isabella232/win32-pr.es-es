---
title: Player.status
description: La propiedad status recupera un valor que indica el estado de Reproductor de Windows Media.
ms.assetid: 781c44d0-15cf-4be2-9e83-76706ce1cb85
keywords:
- Player.status Reproductor de Windows Media
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
ms.openlocfilehash: a03ef010bfcb5ee936183724331e97fac5d6f5912d87c5281a55106519c104e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572054"
---
# <a name="playerstatus"></a>Player.status

La **propiedad status** recupera un valor que indica el estado de Reproductor de Windows Media.

## <a name="syntax"></a>Syntax

*player* . **status**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo lectura.

## <a name="remarks"></a>Comentarios

Los valores contenidos en esta propiedad están sujetos a cambios en cualquier momento y solo se deben usar con fines de presentación.

El **evento StatusChange** se desencadena cada vez que esta propiedad cambia el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media 7.0 o posterior.<br/>                                      |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Player.StatusChange (Evento)**](player-player-statuschange.md)
</dt> </dl>

 

 





