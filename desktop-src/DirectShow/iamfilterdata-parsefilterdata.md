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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989450"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData::P arseFilterData (método)

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
> El encabezado Fil \_ data.h se encuentra en el directorio [Ejemplo del](mapper-sample.md) asignador en la Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamFilterData (interfaz)**](iamfilterdata.md)
</dt> </dl>

 

 




