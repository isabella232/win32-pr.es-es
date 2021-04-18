---
title: IWMPError WebHelp (método)
description: El método WebHelp inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero). | IWMPError WebHelp (método)
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- método WebHelp Windows Media Player
- método WebHelp Windows Media Player, interfaz IWMPError
- Interfaz IWMPError Windows Media Player, método WebHelp
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709182"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError:: WebHelp (método)

El método **WebHelp** inicia la página de ayuda Web de Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores (índice cero).

## <a name="syntax"></a>Sintaxis


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las páginas de ayuda web siempre contienen la información más reciente y más detallada sobre los errores de Windows Media Player. Este método transfiere automáticamente la otra información que necesita la ayuda Web, como la versión del sistema operativo que se está usando.

Para tener acceso directamente a las páginas de ayuda Web, use el código de error y los vínculos del centro de soporte técnico siguientes:

-   [Información del código de error de Windows Media Player](https://support.microsoft.com/kb/886273)
-   [Centro de soluciones de Windows Media Player](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que inicia la página de ayuda Web de Microsoft Windows Media Player en el explorador. El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





