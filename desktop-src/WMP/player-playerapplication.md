---
title: Player. playerApplication
description: La propiedad playerApplication recupera el objeto PlayerApplication cuando se está ejecutando un control remoto de Windows Media Player.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Media Player de Windows Player. playerApplication
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708825"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

La propiedad **playerApplication** recupera el objeto **playerApplication** cuando se está ejecutando un control remoto de Windows Media Player.

## <a name="syntax"></a>Sintaxis

**playerApplication**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **PlayerApplication** de solo lectura o el valor null.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se utiliza cuando la comunicación remota de Windows Media Playercontrol. Si el valor es null, el Playercontrol de Windows Media no se incrusta en modo remoto.

Esta propiedad solo es accesible en código de C++ o en código de script en máscaras a través de la variable global playerApplication.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributos globales**](global-attributes.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





