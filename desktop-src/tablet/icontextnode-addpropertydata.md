---
description: Agrega un fragmento de datos específicos de la aplicación.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: Método IContextNode::AddPropertyData (IACom.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247815"
---
# <a name="icontextnodeaddpropertydata-method"></a>IContextNode::AddPropertyData (método)

Agrega un fragmento de datos específicos de la aplicación.

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

*pPropertyDataId* \[ En\]
</dt> <dd>

Identificador único global (GUID) que se usa para identificar el tipo de datos.

</dd> <dt>

*ulPropertyDataSize* \[ En\]
</dt> <dd>

Tamaño de los datos en bytes.

</dd> <dt>

*pbPropertiesData* \[ En\]
</dt> <dd>

\[in, size \_ is(ulPropertyDataSize)\]

Matriz de enteros de 8 bits sin signo que contiene la información de propiedad que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Observaciones

Use **IContextNode::AddPropertyData para** asociar datos a un nodo de contexto. Para recuperar los datos más adelante, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

El analizador de entrada de lápiz puede eliminar el nodo como parte del análisis de entrada de lápiz, a menos que se confirme el nodo de contexto (vea [**IContextNode::Confirm**](icontextnode-confirm.md)). Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
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

 

 




