---
description: El método GetNextSrc busca en la pista el siguiente origen que aparece en el momento especificado o posterior.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: Método IAMTimelineTrack::GetNextSrc (Qedit.h)
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
ms.openlocfilehash: dd0257fa614a6581cc31f5416e6f1c2395fcb9444721d3668c9f2d2498e52088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904645"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>IamTimelineTrack::GetNextSrc (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetNextSrc` método busca en la pista el siguiente origen que aparece en el momento especificado o posterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj del**](iamtimelineobj.md) objeto de origen.

</dd> <dt>

*Pinout* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio de la búsqueda, en unidades de 100 nanosegundos. Si el método recupera un origen, establece el valor en la hora de detenerse del origen. Si el método no recupera un origen, el valor deja de ser válido y la aplicación no debe usarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S OK si el método recupera un origen o S FALSE en caso \_ \_ contrario.

## <a name="remarks"></a>Comentarios

Si la hora especificada por *pInOut* se encuentra entre las horas de inicio y de detenerse de un origen, el método recupera ese origen.

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

 

 




