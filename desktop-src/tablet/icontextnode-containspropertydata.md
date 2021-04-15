---
description: Determina si el objeto IContextNode contiene datos almacenados en el identificador especificado.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'IContextNode:: ContainsPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497590"
---
# <a name="icontextnodecontainspropertydata-method"></a>IContextNode:: ContainsPropertyData (método)

Determina si el objeto [**IContextNode**](icontextnode.md) contiene datos almacenados en el identificador especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPropertyDataId* \[ de\]
</dt> <dd>

El identificador de los datos.

</dd> <dt>

*pbContains* \[ enuncia\]
</dt> <dd>

**Variante \_ TRUE** si el objeto [**IContextNode**](icontextnode.md) contiene datos almacenados en el identificador especificado; de lo contrario, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Además de los datos específicos de la aplicación, también puede usar este método para determinar si este [**IContextNode**](icontextnode.md) contiene otros datos internos (consulte [propiedades](analysis-hint-properties.md) de la sugerencia de análisis y [propiedades del nodo de contexto](context-node-properties.md)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




