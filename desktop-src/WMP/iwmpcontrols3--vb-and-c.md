---
title: Interfaz IWMPControls3 (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos para la selección del idioma de audio y la compatibilidad que complementan la interfaz IWMPControls2. Además de las propiedades y los métodos heredados de IWMPControls2, la interfaz IWMPControls3 expone las siguientes propiedades.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- Interfaz IWMPControls3 (VB y C) Reproductor de Windows Media
- Interfaz IWMPControls3 (VB y C) Reproductor de Windows Media , descrita
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885012"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>Interfaz IWMPControls3 (VB y C#)

Proporciona propiedades y métodos para la selección del idioma de audio y la compatibilidad que complementan la **interfaz IWMPControls2.**

Además de las propiedades y los métodos heredados de **IWMPControls2,** la **interfaz IWMPControls3** expone las siguientes propiedades.

## <a name="members"></a>Members

La **interfaz IWMPControls3 (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPControls3 (VB y C#)** tiene estos métodos.



| Método                                                                                                         | Descripción                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Devuelve la descripción del idioma de audio correspondiente al índice basado en uno especificado.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Devuelve el LCID de un índice de idioma de audio especificado.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Devuelve el nombre del idioma de audio con el LCID especificado.<br/>                                |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPControls3 (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                                              | Tipo de acceso           | Descripción                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Solo lectura<br/>  | Obtiene el recuento de idiomas de audio admitidos. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Lectura y escritura<br/> | Obtiene o establece el identificador de configuración regional (LCID) del idioma de audio para la reproducción. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Lectura y escritura<br/> | Obtiene o establece el índice basado en uno que corresponde al idioma de audio para la reproducción. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Lectura y escritura<br/> | Obtiene o establece la posición actual en el elemento multimedia actual con un formato de código de hora. Esta propiedad admite actualmente código de tiempo SMPTE. <br/> |



 

Obtenga una **interfaz IWMPControls3** mediante la conversión del valor devuelto por la propiedad [**AxWindowsMediaPlayer.Ctlcontrols.**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls2 (VB y C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





