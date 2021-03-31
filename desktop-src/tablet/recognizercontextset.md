---
description: Comprueba si el objeto InkDivider puede usar la clase InkRecognizerContext para analizar palabras.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: RecognizerContextSet función)
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
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910430"
---
# <a name="recognizercontextset-function"></a>RecognizerContextSet función)

Comprueba si el objeto [**InkDivider**](inkdivider-class.md) puede usar la clase [**InkRecognizerContext**](inkrecognizercontext-class.md) para analizar palabras.

Esta función no está pensada para ser utilizada por el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto [**InkDivider**](inkdivider-class.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *pDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




