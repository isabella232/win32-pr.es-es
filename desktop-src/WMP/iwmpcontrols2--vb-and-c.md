---
title: Interfaz IWMPControls2 (VB y C, Wmp.h)
description: Proporciona un método que complementa la interfaz IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB y C) interfaz de Windows Media Player
- IWMPControls2 (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690424"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Interfaz IWMPControls2 (VB y C#)

Proporciona un método que complementa la interfaz [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .

## <a name="members"></a>Miembros

La interfaz **IWMPControls2 (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMPControls2 (VB y C#)** tiene estos métodos.



| Método                                                           | Descripción                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**pasar**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Mueve el elemento multimedia de vídeo actual al siguiente fotograma o al fotograma anterior e inmoviliza la reproducción.<br/> |



 

En el ejemplo de código siguiente se muestra cómo obtener acceso a una interfaz [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) . El código de ejemplo convierte el valor [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que la propiedad [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) devuelve a un valor **IWMPControls2** .

Para **C#**:


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



Para **VB**:


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





