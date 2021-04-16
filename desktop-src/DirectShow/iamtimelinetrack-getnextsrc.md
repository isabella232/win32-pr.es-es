---
description: El método GetNextSrc busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'IAMTimelineTrack:: GetNextSrc (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679052"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>IAMTimelineTrack:: GetNextSrc (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetNextSrc` método busca en la pista el siguiente origen que aparece en el momento especificado o en una versión posterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSrc* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.

</dd> <dt>

*Patilla* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio de la búsqueda, en unidades de 100-nanosegundos. Si el método recupera un origen, establece el valor en la hora de detención del origen. Si el método no recupera un origen, el valor deja de ser válido y la aplicación no debe usarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el método recupera un origen o s \_ false en caso contrario.

## <a name="remarks"></a>Observaciones

Si la hora especificada por el número de *conexiones* se encuentra entre las horas de inicio y de detención de un origen, el método recupera ese origen.

Si el método devuelve S \_ correcto, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




