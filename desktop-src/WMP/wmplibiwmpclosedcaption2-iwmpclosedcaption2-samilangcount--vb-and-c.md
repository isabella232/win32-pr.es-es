---
title: Propiedad SAMILangCount de IWMPClosedCaption2
description: La propiedad SAMILangCount obtiene el número de idiomas admitidos por el archivo SAMI actual.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Propiedad SAMILangCount Reproductor de Windows Media
- Propiedad SAMILangCount Reproductor de Windows Media , interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Reproductor de Windows Media , propiedad SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900005"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>IWMPClosedCaption2::SAMILangCount, propiedad

La **propiedad SAMILangCount** obtiene el número de idiomas admitidos por el archivo SAMI actual.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el número de idiomas admitidos.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve 0 a menos que un archivo multimedia digital esté abierto (AxWindowsMediaPlayer.openState es igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption (VB y C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMILang (VB y C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPClosedCaption2 (VB y C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2.getSAMILangName (VB y C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





