---
title: IWMPControls2 Step (método)
description: El método Step hace que el elemento multimedia de vídeo actual se desplazará al fotograma siguiente o al fotograma anterior e inmovilizará la reproducción.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- método de paso de Windows Media Player
- método de paso Windows Media Player, interfaz IWMPControls2
- Interfaz IWMPControls2 Windows Media Player, método Step
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690871"
---
# <a name="iwmpcontrols2step-method"></a>IWMPControls2:: Step (método)

El método **Step** hace que el elemento multimedia de vídeo actual se desplazará al fotograma siguiente o al fotograma anterior e inmovilizará la reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lStep* \[ de\]
</dt> <dd>

Un valor **System. Int32** que indica el número de fotogramas que se van a pasar antes de la inmovilización. Debe establecerse en 1 o-1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Actualmente, este método solo admite los parámetros 1 o-1, por lo que solo se puede ejecutar un fotograma cada vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls2 (VB y C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





