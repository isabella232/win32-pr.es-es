---
description: El método GetNextTrans2 recupera la primera transición que aparece en el momento especificado o posterior. Este método es equivalente a IAMTimelineTransable::GetNextTrans, pero toma un valor REFTIME.
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: Método IAMTimelineTransable::GetNextTrans2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c3b1fbc45ca4407e1305704cf40fc82259194d46b270ececf8e5f5d3211b99d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965065"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a>IamTimelineTransable::GetNextTrans2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetNextTrans2` método recupera la primera transición que aparece en el momento especificado o posterior. Este método es equivalente a [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), pero toma un [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTrans* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de transición.

</dd> <dt>

*Pinout* 
</dt> <dd>

Puntero a una variable que especifica el tiempo en segundos. En la entrada, este valor especifica el tiempo desde el que se va a buscar la transición. En la salida, si se recupera una transición, este valor se establece en la hora de detenerse de la transición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si el método recupera una transición o S FALSE si no encuentra una \_ transición. De lo contrario, devuelve **un valor HRESULT** que indica la causa del error.

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

[**IAMTimelineTransable (Interfaz)**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




