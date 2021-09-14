---
description: Agrega un objeto IContextNode a esta colección.
ms.assetid: 48feae05-1cc8-46c3-97cd-4493ee28b8e5
title: Método IContextNodes::AddContextNode (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256754"
---
# <a name="icontextnodesaddcontextnode-method"></a>IContextNodes::AddContextNode (método)

Agrega un [**objeto IContextNode**](icontextnode.md) a esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddContextNode(
  [in] IContextNode *pContextNode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContextNode* \[ En\]
</dt> <dd>

Objeto [**IContextNode**](icontextnode.md) que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




