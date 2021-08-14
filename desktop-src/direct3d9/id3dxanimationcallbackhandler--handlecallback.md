---
description: La aplicación implementa este método. Se llama a este método cuando se produce una devolución de llamada para un conjunto de animación en una de las pistas durante una llamada a ID3DXAnimationController::AdvanceTime.
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: Método ID3DXAnimationCallbackHandler::HandleCallback (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12fcfa0feba1d239cf72c37e78fec63140dda4f954e7c48dffd643dcca4400c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279215"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a>Método ID3DXAnimationCallbackHandler::HandleCallback

La aplicación implementa este método. Se llama a este método cuando se produce una devolución de llamada para un conjunto de animación en una de las pistas durante una llamada a [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista en la que se produce la devolución de llamada.

</dd> <dt>

*pCallbackData* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a datos de devolución de llamada propiedad del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Los valores devueltos de este método los implementa un programador de aplicaciones. En general, si no se produce ningún error, programe el método para devolver D3D \_ OK. De lo contrario, programe el método para devolver un mensaje de error adecuado de [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationCallbackHandler](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
