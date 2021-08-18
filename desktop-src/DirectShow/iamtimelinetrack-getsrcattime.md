---
description: El método GetSrcAtTime recupera el objeto de origen más cercano a la hora especificada, según las condiciones de límite especificadas.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: Método IAMTimelineTrack::GetSrcAtTime (Qedit.h)
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
ms.openlocfilehash: fde7d4d1e1a92c4f403c4d6ae38517bd715cf6d474f22f8a2e262d69fc57139a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052335"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>IamTimelineTrack::GetSrcAtTime (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetSrcAtTime` método recupera el objeto de origen más próximo a la hora especificada, según las condiciones de límite especificadas.

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

*ppSrc* \[ out\]
</dt> <dd>

Recibe un puntero a la [**interfaz IAMTimelineObj**](iamtimelineobj.md) del objeto de origen.

</dd> <dt>

*Time* 
</dt> <dd>

Hora de inicio de la búsqueda, en unidades de 100 nanosegundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Miembro del tipo [**enumerado DE \_ \_ \_ MARCADORES DE BÚSQUEDA DE TRACK DE LA MARCA**](dexterf-track-search-flags.md) DE TRACK DE LA MARCA QUE ESPECIFICA las condiciones de límite para la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | No se ha localizado un objeto de origen.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Se ha localizado un objeto de origen.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>               |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/>      |



 

## <a name="remarks"></a>Comentarios

Si el método devuelve S \_ OK, la **interfaz IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineTrack (interfaz)**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




