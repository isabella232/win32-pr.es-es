---
title: Player.playerApplication
description: La propiedad playerApplication recupera el objeto PlayerApplication cuando se ejecuta un control Reproductor de Windows Media remoto.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Player.playerApplication Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068354"
---
# <a name="playerplayerapplication"></a>Player.playerApplication

La **propiedad playerApplication** recupera el objeto **PlayerApplication** cuando se ejecuta un control Reproductor de Windows Media remoto.

## <a name="syntax"></a>Sintaxis

**playerApplication**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **PlayerApplication de** solo lectura o el valor NULL.

## <a name="remarks"></a>Observaciones

Esta propiedad solo se usa al usar la comunicación remota Windows media playercontrol. Si el valor es NULL, el Windows control del Reproductor de Media no se incrusta en modo remoto.

Esta propiedad solo es accesible en código de C++ o en código de script en máscaras a través de la variable global playerApplication.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Atributos globales**](global-attributes.md)
</dt> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Objeto PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Control remoto del Reproductor de Windows Media**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





