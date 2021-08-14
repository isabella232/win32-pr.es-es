---
description: Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con IContextNode::SavePropertiesData.
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: Método IContextNode::LoadPropertiesData (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d58c37dc91fac9704221fae13505f5e32c6e48d097133e3aad9154f5f2ec3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719679"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>IContextNode::LoadPropertiesData (método)

Vuelve a crear los datos de propiedad internos y específicos de la aplicación para una matriz de bytes que se creó anteriormente con [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cbPropertiesDataSize* \[ En\]
</dt> <dd>

Tamaño de la matriz de datos de propiedades.

</dd> <dt>

*pbPropertiesData* \[ En\]
</dt> <dd>

Matriz de enteros de 8 bits sin signo que contiene información de propiedades que se cargará.

</dd> <dt>

*pfSuccessful* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE** si los datos de propiedad se cargaron correctamente; en caso contrario, **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio xp Tablet PC \[ Edition\]<br/>                                                 |
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

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




