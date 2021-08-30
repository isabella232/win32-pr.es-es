---
description: Obtenga información sobre el método IAMFilterData::P arseFilterData y desempaquete los datos binarios del Registro para un filtro. Esta interfaz está desusada.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Método IAMFilterData::P arseFilterData (Fil \_ data.h)
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
ms.openlocfilehash: b1d3541eb91d4ee2e193db3a81f6524f72b615c029346d84e0c9a4d83e5b57a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965335"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IamFilterData::P arseFilterData (método)

> [!Note]  
> Esta interfaz está desusada. Las nuevas aplicaciones no deben usarla.

 

El `ParseFilterData` método desempaquete los datos binarios del Registro para un filtro.

Normalmente no hay ninguna razón para que una aplicación llame a este método. El [**método IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) proporciona una manera más cómoda de acceder a los datos del Registro de filtro.

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

*rgbFilterData* \[ En\]
</dt> <dd>

Puntero a los datos binarios del Registro. Puede obtener estos datos recuperando la propiedad "FilterData" del moniker de filtro. Los datos se almacenan como **SAFEARRAY** de bytes (VT \_ UI1 \| VT \_ ARRAY).

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Especifica el tamaño de los datos binarios, en bytes.

</dd> <dt>

*prgbRegFilter2* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos desempaquetados. Cuando el método devuelve un resultado, convierte este puntero a un [**tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para tener acceso a los datos del filtro. El autor de la llamada debe liberar la memoria llamando al **método CoTaskMemFree.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve S \_ OK. Si se produce un error, devuelve un código de error.

## <a name="remarks"></a>Comentarios

> [!Note]  
> El encabezado Fil \_ data.h se encuentra en el directorio [Mapper Sample](mapper-sample.md) del SDK Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamFilterData (interfaz)**](iamfilterdata.md)
</dt> </dl>

 

 




