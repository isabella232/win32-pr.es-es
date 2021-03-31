---
description: Establece una función de devolución de llamada que se va a usar durante el reconocimiento de línea.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277392"
---
# <a name="setlinerecocallback-function"></a>SetLineRecoCallback función)

Establece una función de devolución de llamada que se va a usar durante el reconocimiento de línea.

Esta función auxiliar no está pensada para que la use el código de aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDivider* \[ de\]
</dt> <dd>

Identificador del objeto [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*pfn* 
</dt> <dd>

Puntero a una función a la que se llama cuando se produce el reconocimiento en el [**InkDivider**](inkdivider-class.md) que se pasa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ha realizado correctamente.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *pDivider* no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

La siguiente es la sintaxis de la función de devolución de llamada.

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                         |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




