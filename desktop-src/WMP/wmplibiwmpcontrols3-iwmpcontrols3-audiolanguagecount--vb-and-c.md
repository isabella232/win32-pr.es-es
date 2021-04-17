---
title: Propiedad audioLanguageCount de IWMPControls3
description: La propiedad audioLanguageCount obtiene el recuento de idiomas de audio admitidos.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- propiedades de audioLanguageCount Media Player de Windows
- propiedad audioLanguageCount de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad audioLanguageCount
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690870"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a>IWMPControls3:: audioLanguageCount (propiedad)

La propiedad **audioLanguageCount** obtiene el recuento de idiomas de audio admitidos.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el recuento de idiomas de audio admitidos.

## <a name="remarks"></a>Observaciones

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageID (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





