---
description: Agrega una parte de los datos específicos de la aplicación.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'IContextNode:: AddPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ed318520b8ac83acbc8ed615002fababe2a4b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154441"
---
# <a name="icontextnodeaddpropertydata-method"></a>IContextNode:: AddPropertyData (método)

Agrega una parte de los datos específicos de la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPropertyDataId* \[ de\]
</dt> <dd>

Identificador único global (GUID) que se usa para identificar el tipo de datos.

</dd> <dt>

*ulPropertyDataSize* \[ de\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pbPropertiesData* \[ de\]
</dt> <dd>

\[en, el tamaño \_ es (ulPropertyDataSize)\]

Matriz de enteros de 8 bits sin signo que contiene la información de propiedad que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

Use **IContextNode:: AddPropertyData** para asociar datos a un nodo de contexto. Para recuperar los datos más adelante, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).

El analizador de tinta puede eliminar el nodo como parte del análisis de tinta, a menos que se confirme el nodo de contexto (vea [**IContextNode:: CONFIRM**](icontextnode-confirm.md)). Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

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

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




