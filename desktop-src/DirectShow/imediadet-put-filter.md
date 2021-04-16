---
description: El \_ método de filtro Put especifica un filtro de origen para que lo use el detector de medios.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet: método de ut_Filter de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679532"
---
# <a name="imediadetput_filter-method"></a>IMediaDet::p \_ método de filtro UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_Filter` método especifica un filtro de origen para que lo use el detector de medios.

> [!IMPORTANT]
> No agregue el filtro de origen a su propio gráfico de filtros o utilice un filtro que ya esté en un gráfico de filtro. El objeto de detector de medios crea automáticamente un gráfico de filtro interno y el filtro en otro gráfico puede producir resultados inesperados.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Puntero a la interfaz **IUnknown** del filtro de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *newVal* no apunta a un filtro.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo** .<br/>           |



 

## <a name="remarks"></a>Observaciones

Para la mayoría de las aplicaciones, es más sencillo llamar al método [**IMediaDet: \_ :p**](imediadet-put-filename.md) el nombre del archivo de código fuente.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




