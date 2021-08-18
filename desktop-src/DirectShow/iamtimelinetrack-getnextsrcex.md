---
description: El método GetNextSrcEx recupera el siguiente origen después del origen especificado.
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: Método IAMTimelineTrack::GetNextSrcEx (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 438fcdbf4f95406994f5bf0cc63ebf5b5f600a9908419b63c4ceace65dfa9659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952804"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a>IamTimelineTrack::GetNextSrcEx (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetNextSrcEx` método recupera el siguiente origen después del origen especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Plast* 
</dt> <dd>

Puntero al objeto de origen anterior o **NULL** para recuperar el primer origen de la pista.

</dd> <dt>

*ppNext* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del siguiente objeto de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S OK si el método recupera un origen o S FALSE en caso \_ \_ contrario.

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

 

 




