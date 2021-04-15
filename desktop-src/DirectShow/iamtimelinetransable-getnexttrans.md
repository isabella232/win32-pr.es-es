---
description: El método GetNextTrans recupera la primera transición que aparece en el momento especificado o posterior.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable:: GetNextTrans (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689931"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>IAMTimelineTransable:: GetNextTrans (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetNextTrans` método recupera la primera transición que aparece en el momento especificado o posterior.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTrans* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de transición.

</dd> <dt>

*Patilla* 
</dt> <dd>

Puntero a una variable que especifica el tiempo en unidades de 100-nanosegundos. En la entrada, este valor especifica la hora a partir de la que se va a buscar la transición. En la salida, si se recupera una transición, este valor se establece en la hora de detención de la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el método recupera una transición o es \_ false si no encuentra una transición. De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

La hora de inicio de la transición puede ser menor que el tiempo que se especifica en el *pines*, si la transición abarca la hora especificada.

Si el método devuelve S \_ correcto, la interfaz [**IAMTimelineObj**](iamtimelineobj.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




