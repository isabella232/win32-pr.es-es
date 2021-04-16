---
title: Propiedad defaultAudioLanguage de IWMPSettings2
description: La propiedad defaultAudioLanguage obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- propiedades de defaultAudioLanguage Media Player de Windows
- propiedad defaultAudioLanguage de Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, propiedad defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690326"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2::d propiedad efaultAudioLanguage

La propiedad **defaultAudioLanguage** obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el LCID.

## <a name="remarks"></a>Observaciones

Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPControls3. currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





