---
description: Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'IContextNode:: SavePropertiesData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001188"
---
# <a name="icontextnodesavepropertiesdata-method"></a>IContextNode:: SavePropertiesData (método)

Recupera una matriz de bytes que contiene los datos de propiedad internos y específicos de la aplicación para este [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulPropertiesDataSize* \[ in, out\]
</dt> <dd>

Tamaño de la matriz de datos que contiene la información de la propiedad. No se utiliza el valor pasado en.

</dd> <dt>

*ppbPropertiesData* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de propiedad internos y específicos de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Observaciones

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertiesData* cuando ya no necesite la información.

 

Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md). Este método guarda los datos de propiedad que **IInkAnalyzer** ha establecido en [**IContextNode**](icontextnode.md).

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [proxy de datos con análisis de tinta](data-proxy-with-ink-analysis.md).

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

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

