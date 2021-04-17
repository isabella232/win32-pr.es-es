---
title: Interfaz IWMPControls (VB y C) (WMP. h)
description: Proporciona una manera de manipular la reproducción de un elemento multimedia representando los controles de transporte de Windows Media Player, como reproducir, detener y pausar. la interfaz IWMPControls expone las siguientes propiedades.
ms.assetid: 46603d98-c7dd-4c20-a4ae-1472b3af8d52
keywords:
- IWMPControls (VB y C) interfaz de Windows Media Player
- IWMPControls (VB y C) interfaz de Windows Media Player, se describe
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
ms.openlocfilehash: b544978d801f3a9d5d5cbd9644f1d32ac53791e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690427"
---
# <a name="iwmpcontrols-vb-and-c-interface"></a>Interfaz IWMPControls (VB y C#)

Proporciona una manera de manipular la reproducción de un elemento multimedia representando los controles de transporte de Windows Media Player, como reproducir, detener y pausar.

La interfaz **IWMPControls** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPControls (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPControls (VB y C#)** tiene estos métodos.



| Método                                                                       | Descripción                                                                                 |
|:-----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**fastForward**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md) | Inicia la reproducción rápida del elemento multimedia en la dirección de avance.<br/>                     |
| [**fastReverse**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md) | Inicia la reproducción rápida del elemento multimedia en la dirección inversa.<br/>                     |
| [**Nueva**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)               | Establece el elemento siguiente de la lista de reproducción como el elemento actual.<br/>                          |
| [**temporalmente**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)             | Pausa la reproducción del elemento multimedia.<br/>                                               |
| [**reproducción**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)               | Comienza la reproducción del elemento multimedia actual o reanuda la reproducción de un elemento en pausa.<br/> |
| [**playItem**](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)       | Reproduce el elemento multimedia especificado.<br/>                                                  |
| [**previo**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)       | Establece el elemento anterior de la lista de reproducción como el elemento actual.<br/>                      |
| [**detener**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)               | Detiene la reproducción del elemento multimedia.<br/>                                                |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPControls (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso           | Descripción                                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**currentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece el elemento multimedia actual en una lista de reproducción.<br/>                                                                                                                    |
| [**currentMarker**](wmplibiwmpcontrols-iwmpcontrols-currentmarker--vb-and-c.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el número de marcador actual.<br/>                                                                                                                               |
| [**currentPosition**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)<br/>             | Lectura/escritura<br/> | Obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.<br/>                                                                                    |
| [**currentPositionString**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene la posición actual en el elemento multimedia como **System. String**.<br/>                                                                                                   |
| [**isAvailable**](iwmpcontrols-isavailable--vb-and-c.md)<br/>                                        | Solo lectura<br/>  | Obtiene un valor que indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. En C#, este es el método **Get \_ isavailable** .<br/> |



 

Obtenga una interfaz **IWMPControls** con la siguiente propiedad.



| Object                                                                   | Propiedad                                                                   |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls2 (VB y C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





