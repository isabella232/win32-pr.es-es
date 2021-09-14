---
description: El método GetNextSrc2 busca en la pista el siguiente origen que aparece en el momento especificado o posterior. Este método es equivalente a IAMTimelineTrack::GetNextSrc, pero toma un valor REFTIME.
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: Método IAMTimelineTrack::GetNextSrc2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891868"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>IamTimelineTrack::GetNextSrc2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetNextSrc2` método busca en la pista el siguiente origen que aparece en el momento especificado o posterior. Este método es equivalente a [**IAMTimelineTrack::GetNextSrc**](iamtimelinetrack-getnextsrc.md), pero toma un [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
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

En la entrada, contiene la hora de inicio de la búsqueda, en segundos. Si el método recupera un origen, establece el valor en la hora de detenerse del origen. Si el método no recupera un origen, el valor deja de ser válido y la aplicación no debe usarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S OK si el método recupera un origen o S FALSE en caso \_ \_ contrario.

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

[**IamTimelineTrack (interfaz)**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




