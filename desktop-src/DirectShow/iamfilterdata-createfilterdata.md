---
description: Obtenga información sobre el método IAMFilterData::CreateFilterData, que crea datos binarios del Registro para un filtro. Esta interfaz está desusada.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: Método IAMFilterData::CreateFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989460"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IamFilterData::CreateFilterData (método)

> [!Note]  
> Esta interfaz está desusada. Las nuevas aplicaciones no deben usarla.

 

El `CreateFilterData` método crea datos binarios del Registro para un filtro. Estos datos se pueden escribir en el Registro como una subclave REG BINARY denominada FilterData, bajo la clave \_ CLSID del filtro.

Normalmente no hay ninguna razón para que una aplicación llame a este método. El [**método IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automáticamente los datos binarios y los agrega a la ubicación correcta del Registro. Para obtener más información, [vea Cómo registrar filtros de DirectShow.](how-to-register-directshow-filters.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prf2* \[ En\]
</dt> <dd>

Puntero a una [**estructura REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contiene la información del filtro.

</dd> <dt>

*prgbFilterData* \[ out\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos binarios. El método asigna la memoria para los datos. El autor de la llamada debe liberar la memoria llamando al **método CoTaskMemFree.**

</dd> <dt>

*y* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos binarios, en bytes.

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

 

 




