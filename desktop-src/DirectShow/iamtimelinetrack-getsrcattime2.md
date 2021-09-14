---
description: El método GetSrcAtTime2 recupera el objeto de origen más cercano a la hora especificada, según las condiciones de límite especificadas. Este método es equivalente a IAMTimelineTrack::GetSrcAtTime, pero toma un valor REFTIME.
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: Método IAMTimelineTrack::GetSrcAtTime2 (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891844"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a>Método IAMTimelineTrack::GetSrcAtTime2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetSrcAtTime2` método recupera el objeto de origen más cercano a la hora especificada, según las condiciones de límite especificadas. Este método es equivalente a [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), pero toma un [**valor REFTIME.**](reftime.md)

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

*ppSrc* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.

</dd> <dt>

*Time* 
</dt> <dd>

Hora de inicio de la búsqueda, en segundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Miembro del tipo [**enumerado DE MARCAS DE BÚSQUEDA DE TRACK DE LA TRACK \_ \_ \_ DEFIF**](dexterf-track-search-flags.md) que especifica las condiciones de límite para la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | No se ha localizado un objeto de origen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Se ha ubicado un objeto de origen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>               |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>      |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimelineTrack (interfaz)**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




