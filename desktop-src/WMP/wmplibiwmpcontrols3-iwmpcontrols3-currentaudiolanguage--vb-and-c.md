---
title: Propiedad currentAudioLanguage de IWMPControls3
description: La propiedad currentAudioLanguage obtiene o establece el identificador de configuración regional (LCID) del idioma de audio para la reproducción.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- propiedad currentAudioLanguage Reproductor de Windows Media
- Propiedad currentAudioLanguage Reproductor de Windows Media , interfaz IWMPControls3
- Interfaz IWMPControls3 Reproductor de Windows Media , propiedad currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1a4f668cec560528270d52a2abe4777ce32d3ceb38ce21345342ef87866c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115882"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a>Propiedad IWMPControls3::currentAudioLanguage

La **propiedad currentAudioLanguage** obtiene o establece el identificador de configuración regional (LCID) del idioma de audio para la reproducción.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el LCID del idioma de audio.

## <a name="remarks"></a>Comentarios

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

Para Windows contenido basado en multimedia, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Al trabajar con contenido de DVD, la especificación de un LCID hará que se seleccione la primera pista de audio disponible con el identificador de idioma especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.audioLanguageCount (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.currentAudioLanguageIndex (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





