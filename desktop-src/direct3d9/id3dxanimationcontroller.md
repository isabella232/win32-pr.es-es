---
description: Esta interfaz se utiliza para controlar la funcionalidad de animación, conectando los conjuntos de animaciones con los fotogramas de transformación que se animan.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: Interfaz ID3DXAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707960"
---
# <a name="id3dxanimationcontroller-interface"></a>Interfaz ID3DXAnimationController

Esta interfaz se utiliza para controlar la funcionalidad de animación, conectando los conjuntos de animaciones con los fotogramas de transformación que se animan. La interfaz tiene métodos para mezclar varias animaciones y modificar los parámetros de fusión a lo largo del tiempo para permitir transiciones suaves y otros efectos.

## <a name="members"></a>Miembros

La interfaz **ID3DXAnimationController** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationController** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXAnimationController** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Anima la malla y avanza el tiempo de animación global en una cantidad especificada.<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Clona o copia un controlador de animación.<br/>                                                                                                  |
| [**GetAnimationSet**](id3dxanimationcontroller--getanimationset.md)                     | Obtiene un conjunto de animaciones.<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | Obtiene un conjunto de animaciones, dado su nombre.<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Devuelve un identificador de evento de un evento de mezcla de prioridad que se está ejecutando actualmente.<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Devuelve un identificador de evento al evento que se está ejecutando actualmente en la pista de animación especificada.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Obtiene una descripción de un evento de animación especificado.<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Obtiene el número máximo de salidas de animación que puede admitir el controlador de animación.<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Obtiene el número máximo de conjuntos de animaciones que el controlador de animación puede admitir.<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Obtiene el número máximo de eventos que puede admitir el controlador de animación.<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Obtiene el número máximo de pistas en el controlador de animación.<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | Devuelve el número de conjuntos de animación registrados actualmente en el controlador de animación.<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | Obtiene el peso de fusión de la prioridad actual utilizado por el controlador de animación.<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | Obtiene el tiempo de animación global.<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | Obtiene el conjunto de animaciones para la pista especificada.<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | Obtiene la descripción de la pista.<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Devuelve un identificador de evento al siguiente evento de Blend de prioridad programado para que se produzca después de un evento especificado.<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Devuelve un identificador de evento al siguiente evento programado para que se produzca después de un evento especificado en una pista de animación.<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | Establece las claves de evento de mezcla para la pista de animación especificada.<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | Establece una clave de evento que habilita o deshabilita una pista de animación.<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | Establece una clave de evento que cambia la hora local de una pista de animación.<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Establece una clave de evento que cambia la velocidad de reproducción de una pista de animación.<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | Establece una clave de evento que cambia el peso de una pista de animación. El peso se utiliza como multiplicador al combinar varias pistas.<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Agrega una salida de animación al controlador de animación y registra punteros para las transformaciones de escala, rotación y traducción (SRT).<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | Agrega un conjunto de animaciones al controlador de animación.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Restablece el tiempo de la animación global en cero. Los eventos pendientes conservarán las programaciones originales, pero en el nuevo período de tiempo.<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | Establece el peso de fusión de la prioridad usado por el controlador de animación.<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | Aplica la animación establecida a la pista especificada.<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | Establece la descripción de la pista.<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | Habilita o deshabilita una pista en el controlador de animación.<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | Establece la pista en la hora de animación local especificada.<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | Establece el peso de fusión de prioridad para la pista de animación especificada.<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | Establece la velocidad de la pista. La velocidad de la pista es similar a un multiplicador que se usa para acelerar o ralentizar la reproducción de la pista.<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | Establece el peso de la pista. El peso se utiliza para determinar cómo combinar varias pistas.<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Quita todos los eventos de Blend de prioridad programados del controlador de animación.<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Quita todos los eventos de una pista de animación especificada.<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | Quita un evento especificado de una pista de animación, lo que impide la ejecución del evento.<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | Quita un conjunto de animaciones del controlador de animación.<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | Comprueba si un identificador de evento especificado es válido y el evento de animación no se ha completado todavía.<br/>                                              |



 

## <a name="remarks"></a>Observaciones

Cree un objeto de controlador de animación con [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

El tipo LPD3DXANIMATIONCONTROLLER se define como un puntero a la interfaz **ID3DXAnimationController** .


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



El tipo D3DXEVENTHANDLE se define como un identificador de evento para los eventos del controlador de animación.


```
typedef DWORD D3DXEVENTHANDLE;
```



El tipo LPD3DXEVENTHANDLE se define como un puntero a un identificador de evento para los eventos del controlador de animación.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
