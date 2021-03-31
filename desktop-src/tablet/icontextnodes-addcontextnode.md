---
description: Agrega un objeto IContextNode a esta colección.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: 'IContextNodes:: AddContextNode (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.AddContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 18a7438c09fb2a850637bbae549ada61c37fb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154430"
---
# <a name="icontextnodesaddcontextnode-method"></a>IContextNodes:: AddContextNode (método)

Agrega un objeto [**IContextNode**](icontextnode.md) a esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNode* \[ de\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se va a agregar.

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

 

 




