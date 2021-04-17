---
title: Player. openState
description: La propiedad openState recupera un valor que indica el estado del origen de contenido.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Media Player de Windows Player. openState
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
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708214"
---
# <a name="playeropenstate"></a>Player. openState

La propiedad **openState** recupera un valor que indica el estado del origen de contenido.

## <a name="syntax"></a>Sintaxis

*reproductor* . **openState**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**). La constante de enumeración de estilo C se puede derivar prefijando el valor de estado con "wmpos". Por ejemplo, la constante para el estado PlaylistOpening es **wmposPlaylistOpening**.



| Value | Estado                   | Descripción                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | No definido               | Windows Media Player está en un estado indefinido.                                                                                                         |
| 1     | PlaylistChanging        | La nueva lista de reproducción está a punto de cargarse.                                                                                                                    |
| 2     | PlaylistLocating        | Windows Media Player está intentando localizar la lista de reproducción. La lista de reproducción puede ser local (biblioteca o metarchivo con una extensión de nombre de archivo. ASX) o remota. |
| 3     | PlaylistConnecting      | Conectando con la lista de reproducción.                                                                                                                            |
| 4     | PlaylistLoading         | La lista de reproducción se ha encontrado y ahora se está recuperando.                                                                                                    |
| 5     | PlaylistOpening         | La lista de reproducción se ha recuperado y ahora se está analizando y cargando.                                                                                        |
| 6     | PlaylistOpenNoMedia     | La lista de reproducción está abierta.                                                                                                                                      |
| 7     | PlaylistChanged         | Se ha asignado una nueva lista de reproducción a **currentPlaylist**.                                                                                               |
| 8     | MediaChanging           | Se va a cargar un nuevo elemento multimedia.                                                                                                                |
| 9     | MediaLocating           | Windows Media Player está localizando el elemento multimedia. El archivo puede ser local o remoto.                                                                      |
| 10    | MediaConnecting         | Conectando con el servidor que contiene el elemento multimedia.                                                                                                    |
| 11    | MediaLoading            | El elemento multimedia se ha encontrado y ahora se está recuperando.                                                                                                |
| 12    | MediaOpening            | El elemento multimedia se ha recuperado y ahora se está abriendo.                                                                                                 |
| 13    | MediaOpen               | El elemento multimedia está abierto ahora.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Iniciando la adquisición del códec.                                                                                                                            |
| 15    | EndCodecAcquisition     | Se completó la adquisición del códec.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Adquirir una licencia para reproducir contenido protegido con DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | Se ha adquirido una licencia para reproducir contenido protegido con DRM.                                                                                               |
| 18    | BeginIndividualization  | Iniciar la individualización de DRM.                                                                                                                           |
| 19    | EndIndividualization    | Se completó la individualización de DRM.                                                                                                              |
| 20    | MediaWaiting            | Esperando el elemento multimedia.                                                                                                                                |
| 21    | OpeningUnknownURL       | Abrir una dirección URL con un tipo desconocido.                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

No se garantiza que los Estados Media Player de Windows se produzcan en un orden determinado. Además, no todos los Estados se producen necesariamente durante una secuencia de eventos. No debe escribir código que se base en el orden de los Estados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





