---
title: Método de paso IWMPControls2
description: El método step hace que el elemento multimedia de vídeo actual pase al siguiente fotograma o al fotograma anterior y con inmovilizar la reproducción.
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- método step Reproductor de Windows Media
- Método step Reproductor de Windows Media , interfaz IWMPControls2
- Interfaz IWMPControls2 Reproductor de Windows Media , método step
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070747"
---
# <a name="iwmpcontrols2step-method"></a>IWMPControls2::step (método)

El **método step** hace que el elemento multimedia de vídeo actual pase al siguiente fotograma o al fotograma anterior y con inmovilizar la reproducción.

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

*lStep* \[ En\]
</dt> <dd>

Valor **System.Int32** que indica el número de fotogramas que hay que ir paso a paso antes de la inmovilización. Debe establecerse en 1 o -1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Actualmente, este método solo admite los parámetros 1 o -1, por lo que solo puede ir paso a fotograma a la vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls2 (VB y C#)**](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPDVD (VB y C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





