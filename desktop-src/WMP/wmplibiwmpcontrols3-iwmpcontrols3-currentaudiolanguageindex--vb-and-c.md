---
title: Propiedad IWMPControls3 currentAudioLanguageIndex
description: La propiedad currentAudioLanguageIndex obtiene o establece el índice basado en uno que corresponde al idioma de audio para la reproducción.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- propiedad currentAudioLanguageIndex Reproductor de Windows Media
- Propiedad currentAudioLanguageIndex Reproductor de Windows Media interfaz , IWMPControls3
- Interfaz IWMPControls3 Reproductor de Windows Media , propiedad currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c5e17c40908dbc76c61fe60c1b3d885b709d7b1e9282136957e0617ae52ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734995"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a>Propiedad IWMPControls3::currentAudioLanguageIndex

La **propiedad currentAudioLanguageIndex** obtiene o establece el índice basado en uno que corresponde al idioma de audio para la reproducción.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es el índice basado en uno del lenguaje.

## <a name="remarks"></a>Comentarios

Para Windows contenido basado en medios, las propiedades y los métodos relacionados con la selección de idioma solo admiten una única salida.

Use la **propiedad audioLanguageCount** para obtener el número de idiomas de audio admitidos.

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

[**IWMPControls3.currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageDescription (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getAudioLanguageID (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3.getLanguageName (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





