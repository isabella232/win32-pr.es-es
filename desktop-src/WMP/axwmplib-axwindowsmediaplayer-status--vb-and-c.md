---
title: Propiedad AxWindowsMediaPlayer.status
description: La propiedad status obtiene un valor que indica el estado de Reproductor de Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- estado de la propiedad Reproductor de Windows Media
- propiedad status Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864565"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Propiedad AxWindowsMediaPlayer.status

La propiedad status obtiene un valor que indica el estado de Reproductor de Windows Media.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valor de propiedad

System.String que es el estado.

## <a name="remarks"></a>Comentarios

Los valores contenidos en esta propiedad están sujetos a cambios en cualquier momento y solo se deben usar con fines de presentación.

The AxWindowsMediaPlayer. **El evento StatusChange** se desencadena cada vez que esta propiedad cambia de valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer.StatusChange (VB y C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





