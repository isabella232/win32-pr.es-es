---
description: 'El método GetSrcAtTime2 recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas. Este método es equivalente a IAMTimelineTrack:: GetSrcAtTime, pero toma un valor REFTIME.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'IAMTimelineTrack:: GetSrcAtTime2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679159"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a>IAMTimelineTrack:: GetSrcAtTime2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetSrcAtTime2` método recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas. Este método es equivalente a [**IAMTimelineTrack:: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), pero toma un valor [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSrc* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.

</dd> <dt>

*Time* 
</dt> <dd>

Hora de inicio de la búsqueda, en segundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ marcas de \_ búsqueda \_ de DEXTERF Track**](dexterf-track-search-flags.md) que especifica las condiciones de límite de la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                  | Descripción                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | No se encontró un objeto de origen.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Encontró un objeto de origen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>               |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/>      |



 

## <a name="remarks"></a>Observaciones

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

 

 




