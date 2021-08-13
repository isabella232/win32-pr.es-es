---
title: Método de expulsión de IWMPCdrom
description: El método de expulsión expulsa el CD o DVD de la unidad. | Método de expulsión de IWMPCdrom
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- método de Reproductor de Windows Media
- método de Reproductor de Windows Media , interfaz IWMPCdrom
- Interfaz IWMPCdrom Reproductor de Windows Media método de expulsión
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00dbdf22d8eb0ba4073a1b74c25c0d610f3091477e5921dd0856fa835a9bccc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246765"
---
# <a name="iwmpcdromeject-method"></a>IWMPCdrom::dispose (método)

El **método de** expulsión expulsa el CD o DVD de la unidad.

## <a name="syntax"></a>Sintaxis


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la puerta de la unidad está abierta, este método cierra la puerta.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa la** expulsión para abrir la puerta de la unidad de CD o DVD que tiene el índice de cero en respuesta al evento Click de un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.playState (VB y C#)**](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





