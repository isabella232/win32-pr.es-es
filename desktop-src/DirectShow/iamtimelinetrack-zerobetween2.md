---
description: El método ZeroBetween2 quita todo de la pista entre las horas especificadas. Este método es equivalente a IAMTimelineTrack::ZeroBetween, pero toma valores REFTIME.
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: Método IAMTimelineTrack::ZeroBetween2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72ea9d96be976f1b09e1cdc9721eb5eebe7adce2905d7a028d70a9ff50ff58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952784"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>Método IAMTimelineTrack::ZeroBetween2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `ZeroBetween2` método quita todo de la pista entre las horas especificadas. Este método es equivalente a [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Principio del intervalo que se va a borrar, en segundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Final del intervalo que se va a borrar, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                             | Descripción                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El intervalo de tiempo va más allá de todo lo que hay en la pista.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto.<br/>                                             |



 

## <a name="remarks"></a>Comentarios

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

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




