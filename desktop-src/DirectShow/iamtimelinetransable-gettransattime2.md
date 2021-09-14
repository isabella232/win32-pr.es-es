---
description: El método GetTransAtTime2 recupera la transición más cercana a la hora especificada, según las condiciones de límite especificadas. Este método es equivalente a IAMTimelineTransable::GetTransAtTime, pero toma un parámetro REFTIME.
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: Método IAMTimelineTransable::GetTransAtTime2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072191"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>Método IAMTimelineTransable::GetTransAtTime2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetTransAtTime2` método recupera la transición más cercana a la hora especificada, según las condiciones de límite especificadas. Este método es equivalente a [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), pero toma un [**parámetro REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la transición.

</dd> <dt>

*Time* 
</dt> <dd>

Hora a partir de la cual se va a iniciar la búsqueda, en segundos.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Miembro del tipo [**enumerado DE \_ \_ \_ MARCADORES DE BÚSQUEDA DE TRACK DE LA MARCA**](dexterf-track-search-flags.md) DE TRACK DE LA MARCA QUE ESPECIFICA las condiciones de límite para la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | No se encontró ninguna transición.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Se encontró la transición.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/>          |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimelineTransable (interfaz)**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




