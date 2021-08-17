---
description: Establece la propiedad LineHeight en el objeto InkDivider.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Función SetLineHeight
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966824"
---
# <a name="setlineheight-function"></a>Función SetLineHeight

Establece la [**propiedad LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) en el [**objeto InkDivider.**](inkdivider-class.md)

Esta función auxiliar no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ En\]
</dt> <dd>

Identificador del objeto [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*lLineHeight* \[ En\]
</dt> <dd>

Propiedad [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) del objeto [**InkDivider,**](inkdivider-class.md) en unidades HIMETRIC.

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



 

 
