---
description: Agrega un nuevo objeto IInkStrokeDisp al objeto InkDivider que se pasó.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Función AddOneStroke
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247886"
---
# <a name="addonestroke-function"></a>Función AddOneStroke

Agrega un nuevo [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) al [**objeto InkDivider**](inkdivider-class.md) que se pasó.

Esta función no está pensada para que la utilice el código de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ En\]
</dt> <dd>

Identificador del objeto [**InkDivider.**](inkdivider-class.md)

</dd> <dt>

*strokeId* \[ En\]
</dt> <dd>

Identificador [**del**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se va a agregar al [**objeto InkDivider.**](inkdivider-class.md)

</dd> <dt>

*cPoints* \[ En\]
</dt> <dd>

Número de paquetes que forma el nuevo [**objeto IInkStrokeDisp.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*aPoints* \[ En\]
</dt> <dd>

Matriz de paquetes que forma el [**objeto IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en *strokeId*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro hDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




