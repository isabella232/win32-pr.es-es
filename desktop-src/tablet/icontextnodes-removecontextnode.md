---
description: Quita un objeto IContextNode de esta colección.
ms.assetid: ddda506d-4e39-486d-ac7d-211dc7869a73
title: 'IContextNodes:: RemoveContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.RemoveContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 371722cca3d8ccc132c151b37e9d1a469bdb0c3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715223"
---
# <a name="icontextnodesremovecontextnode-method"></a>IContextNodes:: RemoveContextNode (método)

Quita un objeto [**IContextNode**](icontextnode.md) de esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNode* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




