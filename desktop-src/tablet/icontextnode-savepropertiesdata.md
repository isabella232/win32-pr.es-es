---
description: Recupera una matriz de bytes que contiene los datos de propiedades internas y específicos de la aplicación para este IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: Método IContextNode::SavePropertiesData (IACom.h)
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
ms.openlocfilehash: 5b02f5df7526b429a65b2a0baf49bda4571dd718a9bff875c79b7e325de244ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719689"
---
# <a name="icontextnodesavepropertiesdata-method"></a>IContextNode::SavePropertiesData (método)

Recupera una matriz de bytes que contiene los datos de propiedad interna y específicos de la aplicación para [**este IContextNode**](icontextnode.md).

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

Tamaño de la matriz de datos que contiene la información de propiedad. No se usa el valor pasado.

</dd> <dt>

*ppbPropertiesData* \[ out\]
</dt> <dd>

Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de propiedad internos y específicos de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentarios

> [!Caution]  
> Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertiesData* cuando ya no necesite la información.

 

Use este método cuando la aplicación mantenga su propia estructura de datos, que se sincroniza con la de [**IInkAnalyzer**](iinkanalyzer.md). Este método guarda los datos de propiedad que **IInkAnalyzer** ha establecido en [**IContextNode**](icontextnode.md).

Para obtener más información sobre cómo sincronizar los datos de la aplicación con [**IInkAnalyzer**](iinkanalyzer.md), vea [Proxy de datos con análisis de entrada de lápiz.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Consulte también

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

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

