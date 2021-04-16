---
description: El método InsertSpace divide los objetos que existen en el momento especificado e inserta espacio entre ellos.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'IAMTimelineTrack:: InsertSpace (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690120"
---
# <a name="iamtimelinetrackinsertspace-method"></a>IAMTimelineTrack:: InsertSpace (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `InsertSpace` método divide los objetos que existen en el momento especificado e inserta espacio entre ellos.

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

Hora a la que se va a crear la división y el punto inicial del espacio insertado, en unidades de 100-nanosegundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Punto final del espacio insertado, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los posibles valores devueltos se incluyen los siguientes:



| Código devuelto                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | No hay ningún objeto en el momento especificado.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                        |



 

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

 

 




