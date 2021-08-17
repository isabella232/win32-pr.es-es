---
title: Interfaz IWMPCdromRip (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos para administrar la copia o la eliminación de pistas desde un CD de audio.Aescribir un CD mediante la interfaz IWMPCdromRip tiene el mismo efecto que la música de adición mediante la interfaz de usuario Reproductor de Windows Media.
ms.assetid: d7fbfc68-61b5-45bf-8df5-e3125a51a4d8
keywords:
- Interfaz IWMPCdromRip (VB y C) Reproductor de Windows Media
- Interfaz IWMPCdromRip (VB y C) Reproductor de Windows Media , descrito
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
ms.openlocfilehash: 98a418f71ad8605e81115fa9ef1a45488a6830db94c260ef60aa0d991724d80a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747941"
---
# <a name="iwmpcdromrip-vb-and-c-interface"></a>Interfaz IWMPCdromRip (VB y C#)

Proporciona propiedades y métodos para administrar la copia o *eliminación de* pistas desde un CD de audio.

El uso de la interfaz **IWMPCdromRip** de un CD tiene el mismo efecto que la música de arras mediante Reproductor de Windows Media interfaz de usuario. El contenido desmesado se agrega automáticamente a la biblioteca según las preferencias del usuario. Para obtener más información sobre las preferencias del usuario para la ala de CD, vea " Alegar música de CDs" en Reproductor de Windows Media Ayuda.

La **interfaz IWMPCdromRip** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPCdromRip (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPCdromRip (VB y C#)** tiene estos métodos.



| Método                                                                 | Descripción                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| [**startRip**](wmplibiwmpcdromrip-iwmpcdromrip-startrip--vb-and-c.md) | Arranca el CD.<br/>                  |
| [**stopRip**](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)   | Detiene el proceso de esión de CD.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPCdromRip (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                | Tipo de acceso          | Descripción                                                                                   |
|:----------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**ripProgress**](wmplibiwmpcdromrip-iwmpcdromrip-ripprogress--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el progreso de la instalación de CD como porcentaje completado.<br/>                                  |
| [**ripState**](wmplibiwmpcdromrip-iwmpcdromrip-ripstate--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor de enumeración que indica el estado actual del proceso de unmanaged.<br/> |



 

Obtenga una **interfaz IWMPCdromRip** mediante la conversión de la interfaz **IWMPCdrom** del CD que desea extraer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Arrasar un CD**](ripping-a-cd.md)
</dt> </dl>

 

 





