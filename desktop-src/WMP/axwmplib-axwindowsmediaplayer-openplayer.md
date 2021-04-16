---
title: AxWindowsMediaPlayer. openPlayer, método
description: El método openPlayer abre Windows Media Player mediante la dirección URL especificada. | AxWindowsMediaPlayer. openPlayer, método
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- método openPlayer de Windows Media Player
- método openPlayer de Windows Media Player, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, método openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699398"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>AxWindowsMediaPlayer. openPlayer, método

El método **openPlayer** abre Windows Media Player mediante la dirección URL especificada.

## <a name="syntax"></a>Sintaxis


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System. String** que es la dirección URL del elemento multimedia que se va a reproducir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método inicia Windows Media Player con la dirección URL especificada como elemento multimedia actual. Si el reproductor se cerró previamente en modo de máscara, se abrirá con la última máscara elegida por el usuario. De lo contrario, el reproductor se abre en modo completo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





