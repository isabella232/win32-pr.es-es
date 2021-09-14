---
description: El método SetStartStop2 establece las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto. Este método es equivalente a IAMTimelineObj::SetStartStop, pero toma valores REFTIME.
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: Método IAMTimelineObj::SetStartStop2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973802"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>Método IAMTimelineObj::SetStartStop2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetStartStop2` método establece las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto. Este método es equivalente a [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Nueva hora de inicio, en segundos o –1 para mantener la hora de inicio existente.

</dd> <dt>

*Detención* 
</dt> <dd>

Nueva hora de detenerse, en segundos o –1 para mantener la hora de detenerse existente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                  | Descripción                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argumento no válido.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Sin implementar.<br/>  |



 

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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




