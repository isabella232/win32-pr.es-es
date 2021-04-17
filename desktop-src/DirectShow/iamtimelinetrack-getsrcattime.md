---
description: El método GetSrcAtTime recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'IAMTimelineTrack:: GetSrcAtTime (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690121"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>IAMTimelineTrack:: GetSrcAtTime (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetSrcAtTime` método recupera el objeto de origen más cercano a la hora especificada, de acuerdo con las condiciones de límite especificadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
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

Hora de inicio de la búsqueda, en unidades de 100-nanosegundos.

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

 

 




