---
description: 'Nota: esta interfaz está en desuso.'
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData:: CreateFilterData (método) (Fil \_ Data. h)'
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
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679394"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IAMFilterData:: CreateFilterData (método)

> [!Note]  
> Esta interfaz está desusada. Las nuevas aplicaciones no deben utilizarla.

 

El `CreateFilterData` método crea datos binarios del registro para un filtro. Estos datos se pueden escribir en el registro como una \_ subclave reg binaria denominada FilterData, en la clave CLSID del filtro.

Normalmente no hay ningún motivo para que una aplicación llame a este método. El método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automáticamente los datos binarios y los agrega a la ubicación correcta en el registro. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).

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

*PRF2* \[ de\]
</dt> <dd>

Puntero a una estructura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contiene la información del filtro.

</dd> <dt>

*prgbFilterData* \[ enuncia\]
</dt> <dd>

Dirección de una variable que recibe un puntero a los datos binarios. El método asigna la memoria para los datos. El llamador debe liberar la memoria mediante una llamada al método **CoTaskMemFree** .

</dd> <dt>

*PCB* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el tamaño de los datos binarios, en bytes.

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

 

 




