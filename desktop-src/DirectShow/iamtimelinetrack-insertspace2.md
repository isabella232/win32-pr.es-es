---
description: El método InsertSpace2 divide los objetos que existen en el momento especificado e inserta espacio entre ellos. Este método es equivalente a IAMTimelineTrack::InsertSpace, pero toma valores REFTIME.
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: Método IAMTimelineTrack::InsertSpace2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f851e6bdccb755977210fcd67e7ce0bb6cb270ec3ff6a4f1fed4806a035a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052255"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>IamTimelineTrack::InsertSpace2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método divide los objetos que existen en el momento especificado e `InsertSpace2` inserta espacio entre ellos. Este método es equivalente a [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Hora a la que se va a crear la división y el punto inicial del espacio insertado, en segundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Punto final del espacio insertado, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores devueltos posibles se incluyen los siguientes:



| Código devuelto                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | No hay objetos en el momento especificado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                        |



 

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

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




