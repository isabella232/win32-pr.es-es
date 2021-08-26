---
description: Comprueba si el objeto InkDivider puede usar la clase InkRecognizerContext para analizar palabras.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Función RecognizerContextSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: fee6fa3f9f9743f048cab4d9bee5af3fa9215ca903227acd0aa67cb68037550d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934715"
---
# <a name="recognizercontextset-function"></a>Función RecognizerContextSet

Comprueba si el [**objeto InkDivider**](inkdivider-class.md) puede usar la [**clase InkRecognizerContext**](inkrecognizercontext-class.md) para analizar palabras.

Esta función no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ En\]
</dt> <dd>

Identificador del objeto [**InkDivider.**](inkdivider-class.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro pDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




