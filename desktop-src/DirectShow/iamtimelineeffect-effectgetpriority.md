---
description: El método EffectGetPriority recupera el nivel de prioridad del efecto. Para un objeto determinado, el motor de representación aplica efectos en orden de prioridad, empezando por el nivel de prioridad cero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: Método IAMTimelineEffect::EffectGetPriority (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892124"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a>IamTimelineEffect::EffectGetPriority (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `EffectGetPriority` método recupera el nivel de prioridad del efecto. Para un objeto determinado, el motor de representación aplica efectos en orden de prioridad, empezando por el nivel de prioridad cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe el nivel de prioridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

[**IAMTimelineEffect (interfaz)**](iamtimelineeffect.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




