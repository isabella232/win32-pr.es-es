---
description: Recupera el identificador de trazo del trazo al que hace referencia un valor de índice dentro del objeto IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: Método IContextNode::GetStrokeId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f3eb5408ff9f6d2b98acebc3f6e936165ea46132fa1fdda252da8797b864c8c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590725"
---
# <a name="icontextnodegetstrokeid-method"></a>IContextNode::GetStrokeId (método)

Recupera el identificador de trazo del trazo al que hace referencia un valor de índice dentro del [**objeto IContextNode.**](icontextnode.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulIndex* \[ En\]
</dt> <dd>

Índice del trazo que se va a devolver.

</dd> <dt>

*plStrokeId* \[ out\]
</dt> <dd>

Identificador de trazo del trazo al que hace referencia el *parámetro ulIndex* dentro del [**objeto IContextNode**](icontextnode.md) actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**IContextNode::GetStrokeCount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




