---
title: Propiedad AxWindowsMediaPlayer. status
description: La propiedad status obtiene un valor que indica el estado de Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- propiedades de estado de Windows Media Player
- propiedad status Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad status
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
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699703"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Propiedad AxWindowsMediaPlayer. status

La propiedad status obtiene un valor que indica el estado de Windows Media Player.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Valor de propiedad

System. String que es el estado.

## <a name="remarks"></a>Observaciones

Los valores contenidos en esta propiedad están sujetos a cambios en cualquier momento y deben usarse solo con fines de presentación.

AxWindowsMediaPlayer. El evento **StatusChange** se desencadena cuando esta propiedad cambia el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Evento AxWindowsMediaPlayer. StatusChange (VB y C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





