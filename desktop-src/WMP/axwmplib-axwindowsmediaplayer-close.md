---
title: Método AxWindowsMediaPlayer.close
description: El método close cierra el archivo multimedia digital actual, detiene la reproducción en Reproductor de Windows Media y libera Reproductor de Windows Media recursos.
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- método close Reproductor de Windows Media
- método close Reproductor de Windows Media clase , AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media método , close
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cece6f4034a687a68cbd596bfe26a23c2fe70112c9e432c6f06b9065c1436c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737094"
---
# <a name="axwindowsmediaplayerclose-method"></a>Método AxWindowsMediaPlayer.close

El método close cierra el archivo multimedia digital actual, detiene la reproducción en Reproductor de Windows Media y libera Reproductor de Windows Media recursos.

## <a name="syntax"></a>Sintaxis


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método cierra el archivo multimedia digital actual, no Reproductor de Windows Media sí mismo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que, al hacer clic en él, detiene la reproducción en Reproductor de Windows Media y libera los recursos en uso. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





