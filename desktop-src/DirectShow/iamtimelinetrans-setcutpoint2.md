---
description: El método SetCutPoint2 establece la hora a la que la transición se reduce de un origen al siguiente, si la transición se representa como un corte. Este método es equivalente a IAMTimelineTrans::SetCutPoint, pero toma un valor REFTIME.
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: Método IAMTimelineTrans::SetCutPoint2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9d4dedfb31efab45f56229e2dd4db10fc9e43defe822662bc2d7be06f0c1a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502345"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>Método IAMTimelineTrans::SetCutPoint2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método establece la hora a la que la transición se reduce de un origen al siguiente, si la transición `SetCutPoint2` se representa como un corte. Este método es equivalente a [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), pero toma un [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TLTime* 
</dt> <dd>

Punto de corte con respecto al inicio de la transición, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

[**IamTimelineTrans (interfaz)**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




