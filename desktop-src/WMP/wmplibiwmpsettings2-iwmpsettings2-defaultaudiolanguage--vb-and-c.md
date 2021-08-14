---
title: Propiedad IWMPSettings2 defaultAudioLanguage
description: La propiedad defaultAudioLanguage obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Reproductor de Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- propiedad defaultAudioLanguage Reproductor de Windows Media
- Propiedad defaultAudioLanguage Reproductor de Windows Media , interfaz IWMPSettings2
- Interfaz IWMPSettings2 Reproductor de Windows Media , propiedad defaultAudioLanguage
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
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331105"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>Propiedad IWMPSettings2::d efaultAudioLanguage

La **propiedad defaultAudioLanguage** obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Reproductor de Windows Media.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es el LCID.

## <a name="remarks"></a>Comentarios

Un LCID identifica de forma única un dialecto de idioma determinado, denominado configuración regional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPControls3.currentAudioLanguage (VB y C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings2 (VB y C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





