---
description: El método SetWindowForeground mueve la ventana de vídeo al primer plano y, opcionalmente, le proporciona el foco.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Método CBaseControlWindow.SetWindowForeground (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255578"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a>CBaseControlWindow.SetWindowForeground (método)

El `SetWindowForeground` método mueve la ventana de vídeo al primer plano y, opcionalmente, le proporciona el foco.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Foco* 
</dt> <dd>

Valor que especifica si la ventana de vídeo recibirá el foco. Un valor de 1 proporciona el foco de la ventana y 0 no.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                           | Descripción                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NOERROR**</dt> </dl>                | El método se ha llevado a cabo de forma correcta.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | El foco no es igual a 1 o 0.<br/>                                   |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El filtro actual no está conectado a un gráfico de filtros completo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




