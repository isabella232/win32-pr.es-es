---
title: Player.openState
description: La propiedad openState recupera un valor que indica el estado del origen de contenido.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player.openState Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c0b88d3cab5d5bae4efb1e9a2a5032709943d82484b073302bf0b45a6f5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995985"
---
# <a name="playeropenstate"></a>Player.openState

La **propiedad openState** recupera un valor que indica el estado del origen de contenido.

## <a name="syntax"></a>Syntax

*player* . **openState**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**). La constante de enumeración de estilo C se puede derivar anteponer el valor de estado a "wmpos". Por ejemplo, la constante para el estado PlaylistOpening es **wmposPlaylistOpening.**



| Value | Estado                   | Descripción                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No definido               | Reproductor de Windows Media está en un estado indefinido.                                                                                                         |
| 1     | PlaylistChanging        | La nueva lista de reproducción está a punto de cargarse.                                                                                                                    |
| 2     | PlaylistLocating        | Reproductor de Windows Media está intentando localizar la lista de reproducción. La lista de reproducción puede ser local (biblioteca o metarchivo con una extensión de nombre de archivo .asx) o remota. |
| 3     | PlaylistConnecting      | Conectarse a la lista de reproducción.                                                                                                                            |
| 4     | PlaylistLoading         | Se ha encontrado la lista de reproducción y ahora se está recuperando.                                                                                                    |
| 5     | Lista de reproducciónAbrir         | La lista de reproducción se ha recuperado y ahora se está analizando y cargando.                                                                                        |
| 6     | Lista de reproducciónAbrirNoMedia     | La lista de reproducción está abierta.                                                                                                                                      |
| 7     | PlaylistChanged         | Se ha asignado una nueva lista de reproducción a **currentPlaylist.**                                                                                               |
| 8     | MediaChanging           | Un nuevo elemento multimedia está a punto de cargarse.                                                                                                                |
| 9     | MediaLocating           | Reproductor de Windows Media está localizando el elemento multimedia. El archivo puede ser local o remoto.                                                                      |
| 10    | MediaConnecting         | Conectarse al servidor que contiene el elemento multimedia.                                                                                                    |
| 11    | MediaLoading            | Se ha ubicado el elemento multimedia y ahora se está recuperando.                                                                                                |
| 12    | MediaOpening            | Se ha recuperado el elemento multimedia y ahora se está abierto.                                                                                                 |
| 13    | MediaOpen               | El elemento multimedia ya está abierto.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Inicio de la adquisición de códecs.                                                                                                                            |
| 15    | EndCodecAcquisition     | La adquisición de códecs se ha completado.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Adquirir una licencia para reproducir contenido protegido con DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | Se ha adquirido la licencia para reproducir contenido protegido con DRM.                                                                                               |
| 18    | BeginIndividualization  | Iniciar la individualización de DRM.                                                                                                                           |
| 19    | EndIndividualization    | Se ha completado la individualización de DRM.                                                                                                              |
| 20    | MediaWaiting            | Esperando el elemento multimedia.                                                                                                                                |
| 21    | OpeningUnknownURL       | Abrir una dirección URL con un tipo desconocido.                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

Reproductor de Windows Media se garantiza que los estados se produzcan en un orden determinado. Además, no todos los estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player.OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





