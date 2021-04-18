---
title: Interfaz IWMPCdromRip (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para administrar las pistas de copia de un CD de audio, o la copia desde ella. la copia desde CD mediante la interfaz IWMPCdromRip tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- IWMPCdromRip (VB y C) interfaz de Windows Media Player
- IWMPCdromRip (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPCdromRip (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d069fd8bd727d6a2a380c2ef29ce7c086db88d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690430"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interfaz IWMPCdromRip (VB y C#)

Proporciona propiedades y métodos para administrar las pistas de *copia o copia desde un* CD de audio.

La copia desde CD mediante la interfaz **IWMPCdromRip** tiene el mismo efecto que la copia de música mediante la interfaz de usuario de Windows Media Player. El contenido copiado se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información acerca de las preferencias de usuario para la copia desde CD, consulte "copiar música desde CDs" en la ayuda de Windows Media Player.

La interfaz **IWMPCdromRip** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPCdromRip (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPCdromRip (VB y C#)** tiene estos métodos.



| Método                                                                 | Descripción                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | RIP el CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Detiene el proceso de copia de CD.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPCdromRip (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                | Tipo de acceso          | Descripción                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el progreso de la copia de CD como porcentaje completado.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor de enumeración que indica el estado actual del proceso de copia desde CD.<br/> |



 

Obtenga una interfaz **IWMPCdromRip** mediante la conversión de la interfaz **IWMPCdrom** del CD que desea copiar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Copia desde CD**](ripping-a-cd.md)
</dt> </dl>

 

 





