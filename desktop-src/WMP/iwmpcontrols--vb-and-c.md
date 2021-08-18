---
title: Interfaz IWMPControls (VB y C) (Wmp.h)
description: Proporciona una manera de manipular la reproducción de un elemento multimedia mediante la representación de los controles de transporte de Reproductor de Windows Media, como Reproducir, Detener y Pausa. La interfaz IWMPControls expone las siguientes propiedades.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- Interfaz IWMPControls (VB y C) Reproductor de Windows Media
- Interfaz IWMPControls (VB y C) Reproductor de Windows Media , descrita
topic_type:
- apiref
api_name:
- IWMPControls (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b96f79b8942935d9722bf38dbd1ae946b03d16496664b4c069552819785c1f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119314"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Interfaz IWMPControls (VB y C#)

Proporciona una manera de manipular la reproducción de un elemento multimedia mediante la representación de los controles de transporte de Reproductor de Windows Media, como Reproducir, Detener y Pausar.

La **interfaz IWMPControls** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPControls (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPControls (VB y C#)** tiene estos métodos.



| Método                                                                       | Descripción                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**fastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Inicia el juego rápido del elemento multimedia en la dirección de avance.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Inicia el juego rápido del elemento multimedia en la dirección inversa.<br/>                     |
| [**próximo**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Establece el siguiente elemento de la lista de reproducción como el elemento actual.<br/>                          |
| [**Pausa**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Pausa la reproducción del elemento multimedia.<br/>                                               |
| [**Jugar**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Reproduce el elemento multimedia especificado.<br/>                                                  |
| [**Anterior**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Establece el elemento anterior de la lista de reproducción como el elemento actual.<br/>                      |
| [**Parada**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Detiene la reproducción del elemento multimedia.<br/>                                                |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPControls (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el elemento multimedia actual en una lista de reproducción.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el número de marcador actual.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene la posición actual en el elemento multimedia como **System.String**.<br/>                                                                                                   |
| [**Isavailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Solo lectura<br/>  | Obtiene un valor que indica si un tipo especificado de información está disponible o si se puede realizar una acción especificada. En C#, este es el **método \_ get isAvailable.**<br/> |



 

Obtenga una **interfaz IWMPControls** mediante la siguiente propiedad.



| Object                                                                   | Propiedad                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls2 (VB y C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





