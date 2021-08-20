---
title: Método IWMPControls3 getAudioLanguageDescription
description: El método getAudioLanguageDescription devuelve la descripción del idioma de audio correspondiente al índice basado en uno especificado.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- Método getAudioLanguageDescription Reproductor de Windows Media
- Método getAudioLanguageDescription Reproductor de Windows Media , interfaz IWMPControls3
- Interfaz IWMPControls3 Reproductor de Windows Media , método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1172fd119671a8452ac581d3c3a27efd890456cec98f1ef8d6e61340a54c4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861875"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a>IWMPControls3::getAudioLanguageDescription (método)

El **método getAudioLanguageDescription** devuelve la descripción del idioma de audio correspondiente al índice basado en uno especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de lenguaje de audio basado en uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es la descripción del idioma de audio.

## <a name="remarks"></a>Comentarios

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Use la **propiedad audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**IWMPControls3.currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





