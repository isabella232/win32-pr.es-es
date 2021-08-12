---
title: Interfaz IWMPControls2 (VB y C, Wmp.h)
description: Proporciona un método que complementa la interfaz IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- Interfaz IWMPControls2 (VB y C) Reproductor de Windows Media
- Interfaz IWMPControls2 (VB y C) Reproductor de Windows Media , descrita
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
ms.openlocfilehash: 9757471526eb385168a10c505254b5a418ea7f9811576de95266c06817c73109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575925"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a>Interfaz IWMPControls2 (VB y C#)

Proporciona un método que complementa la [**interfaz IWMPControls.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)

## <a name="members"></a>Miembros

La **interfaz IWMPControls2 (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMPControls2 (VB y C#)** tiene estos métodos.



| Método                                                           | Descripción                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Paso**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | Mueve el elemento multimedia de vídeo actual al fotograma siguiente o al fotograma anterior y inmoviliza la reproducción.<br/> |



 

En el código de ejemplo siguiente se muestra cómo acceder a una [**interfaz IWMPControls2.**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) El código de ejemplo convierte el [**valor IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) que la propiedad [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) devuelve a un **valor IWMPControls2.**

Para **C#:**


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
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls3 (VB y C#)**](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





