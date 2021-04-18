---
title: IWMPControls3 getAudioLanguageID, método
description: El método getAudioLanguageID devuelve el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- método getAudioLanguageID de Windows Media Player
- método getAudioLanguageID Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650138"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>IWMPControls3:: getAudioLanguageID (método)

El método **getAudioLanguageID** devuelve el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ de\]
</dt> <dd>

**System. Int32** que es el índice de base uno del lenguaje de audio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Int32** que es el LCID.

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.

En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.

Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.

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

[**IWMPControls3. audioLanguageCount (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





