---
description: El método FixTimes2 redondea las horas de inicio y de detenerse especificadas a los límites de fotogramas más cercanos, tal como se define en la configuración de velocidad de fotogramas del grupo primario. Este método es equivalente a IAMTimelineObj::FixTimes, pero toma valores REFTIME.
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: Método IAMTimelineObj::FixTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892004"
---
# <a name="iamtimelineobjfixtimes2-method"></a>IamTimelineObj::FixTimes2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método redondea las horas de inicio y de detenerse especificadas a los límites de fotogramas más cercanos, tal como se define en la configuración de velocidad de fotogramas del grupo `FixTimes2` primario. Este método es equivalente a [**IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md)pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio, en segundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que contiene el tiempo de detenerse, en segundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E \_ NOTINTREE si el objeto no forma parte de un grupo.

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

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




