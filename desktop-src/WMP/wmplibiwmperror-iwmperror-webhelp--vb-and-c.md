---
title: Método webHelp de IWMPError
description: El método webHelp inicia la página Reproductor de Windows Media Web Help para mostrar más información sobre el primer error en la cola de errores (índice cero). | Método webHelp de IWMPError
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- Método webHelp Reproductor de Windows Media
- Método webHelp Reproductor de Windows Media , interfaz IWMPError
- Interfaz IWMPError Reproductor de Windows Media , método webHelp
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465713"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError::webHelp (método)

El **método webHelp** inicia la Reproductor de Windows Media web para mostrar más información sobre el primer error en la cola de errores (índice cero).

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

Las páginas de Ayuda web siempre contienen la información más reciente y más detallada sobre Reproductor de Windows Media errores. Este método transfiere automáticamente la otra información necesaria para la Ayuda web, como la versión del sistema operativo que se usa.

Para acceder directamente a las páginas de Ayuda web, use el código de error siguiente y los vínculos del Centro de soporte técnico:

-   [Reproductor de Windows Media Información del código de error](https://support.microsoft.com/kb/886273)
-   [Reproductor de Windows Media Centro de soluciones](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un botón que inicia la Reproductor de Windows Media Web Help de Microsoft en el explorador. El objeto AxWMPLib.AxWindowsMediaPlayer se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> </dl>

 

 





