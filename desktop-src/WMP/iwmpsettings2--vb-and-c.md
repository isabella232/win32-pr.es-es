---
title: Interfaz IWMPSettings2 (VB y C) (Wmp.h)
description: Proporciona propiedades y un método que complementan la interfaz IWMPSettings. Además de las propiedades y los métodos heredados de IWMPSettings, la interfaz IWMPSettings2 expone las siguientes propiedades.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- Interfaz IWMPSettings2 (VB y C) Reproductor de Windows Media
- Interfaz IWMPSettings2 (VB y C) Reproductor de Windows Media , descrita
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e227cc255eee625df926031369ef8be0fe270e377b143adff2c3ed2d9ab0aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135361"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>Interfaz IWMPSettings2 (VB y C#)

Proporciona propiedades y un método que complementan la **interfaz IWMPSettings.**

Además de las propiedades y los métodos heredados de **IWMPSettings,** la **interfaz IWMPSettings2** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPSettings2 (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPSettings2 (VB y C#)** tiene estos métodos.



| Método                                                                                                   | Descripción                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Solicita un nivel de acceso especificado a la biblioteca.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPSettings2 (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                                    | Tipo de acceso          | Descripción                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor que indica los permisos concedidos actualmente para el acceso a la biblioteca. <br/> |



 

Obtenga una **interfaz IWMPSettings2** mediante la conversión del valor devuelto por la **propiedad AxWindowsMediaPlayer.settings.**



| Object                                                                   | Propiedad                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Configuración**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





