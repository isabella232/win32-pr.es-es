---
description: El método InsertSpace divide los objetos que existen en el momento especificado e inserta espacio entre ellos.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: Método IAMTimelineTrack::InsertSpace (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891841"
---
# <a name="iamtimelinetrackinsertspace-method"></a>IamTimelineTrack::InsertSpace (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método divide los objetos que existen en el momento especificado e `InsertSpace` inserta espacio entre ellos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Hora a la que se va a crear la división y el punto inicial del espacio insertado, en unidades de 100 nanosegundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Punto final del espacio insertado, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores devueltos posibles se incluyen los siguientes:



| Código devuelto                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | No hay objetos en el momento especificado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                        |



 

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

 

 




