---
description: Elimina un objeto InkDivider y libera los recursos asociados.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: DeleteInkDivider función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912353"
---
# <a name="deleteinkdivider-function"></a>DeleteInkDivider función)

Elimina un objeto [**InkDivider**](inkdivider-class.md) y libera los recursos asociados.

Esta función no está pensada para ser utilizada por el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI DeleteInkDivider(
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
| <dl> <dt>**S \_ correcto**</dt> </dl>         | El método se ha llevado a cabo de forma correcta.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *hDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




