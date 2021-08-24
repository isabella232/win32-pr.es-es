---
description: Quita un fragmento de datos específicos de la aplicación.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: Método IContextNode::RemovePropertyData (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cba88c90f33a52e0a1ff94cdbe69e2f210163769a09916f04de41c262d9e7e22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660715"
---
# <a name="icontextnoderemovepropertydata-method"></a>IContextNode::RemovePropertyData (método)

Quita un fragmento de datos específicos de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPropertyDataId* \[ En\]
</dt> <dd>

Identificador de los datos que se quitarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

**E \_ Se devuelve INVALIDARG** si el *parámetro pPropertyDataId* es una de las constantes [de propiedades del nodo de](context-node-properties.md) contexto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




