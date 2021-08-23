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
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995855"
---
# <a name="playerplayerapplication"></a>Player.playerApplication

La **propiedad playerApplication** recupera el objeto **PlayerApplication** cuando se ejecuta un control Reproductor de Windows Media remoto.

## <a name="syntax"></a>Syntax

**playerApplication**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un objeto **PlayerApplication de** solo lectura o el valor NULL.

## <a name="remarks"></a>Comentarios

Esta propiedad solo se usa cuando se usa la comunicación remota Windows control del Reproductor de Media. Si el valor es NULL, el Windows control del Reproductor de Media no se incrusta en modo remoto.

Esta propiedad solo es accesible en código de C++ o en código de script en máscaras a través de la variable global playerApplication.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/>                                 |
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

 

 





