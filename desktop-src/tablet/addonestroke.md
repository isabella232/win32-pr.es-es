---
description: Agrega un nuevo objeto IInkStrokeDisp al objeto InkDivider que se ha pasado.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496751"
---
# <a name="addonestroke-function"></a>AddOneStroke función)

Agrega un nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) al objeto [**InkDivider**](inkdivider-class.md) que se ha pasado.

Esta función no está pensada para ser utilizada por el código de la aplicación.

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

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*strokeId* \[ de\]
</dt> <dd>

[**Identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) del objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se va a agregar al objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*cPoints* \[ de\]
</dt> <dd>

El número de paquetes que componen el nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*aPoints* \[ de\]
</dt> <dd>

La matriz de paquetes que componen el objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en *strokeId*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *hDivider* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




