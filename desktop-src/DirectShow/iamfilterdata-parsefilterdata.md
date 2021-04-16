---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData::P método arseFilterData (Fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679393"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData::P método arseFilterData

> [!Note]  
> Esta interfaz está desusada. Las nuevas aplicaciones no deben utilizarla.

 

El `ParseFilterData` método desempaqueta los datos binarios del registro para un filtro.

Normalmente no hay ningún motivo para que una aplicación llame a este método. El método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) proporciona una manera más cómoda de acceder a los datos del registro del filtro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rgbFilterData* \[ de\]
</dt> <dd>

Puntero a los datos del registro binarios. Puede obtener estos datos recuperando la propiedad "FilterData" del moniker del filtro. Los datos se almacenan como una **SAFEARRAY** de bytes ( \_ matriz de VT UI1 \| VT \_ ).

</dd> <dt>

*CB* \[ de\]
</dt> <dd>

Especifica el tamaño de los datos binarios, en bytes.

</dd> <dt>

*prgbRegFilter2* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos desempaquetados. Cuando el método devuelve, convierte este puntero en un tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para tener acceso a los datos del filtro. El llamador debe liberar la memoria mediante una llamada al método **CoTaskMemFree** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve S \_ correcto. Si se produce un error, devuelve un código de error.

## <a name="remarks"></a>Observaciones

> [!Note]  
> El encabezado Fil \_ Data. h se encuentra en el directorio de [ejemplo del asignador](mapper-sample.md) en el Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Fil \_ Data. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




