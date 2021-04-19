---
description: 'El método SetCutPoint2 establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte. Este método es equivalente a IAMTimelineTrans:: SetCutPoint, pero toma un valor REFTIME.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'IAMTimelineTrans:: SetCutPoint2 (método) (QEDIT. h)'
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
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690043"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>IAMTimelineTrans:: SetCutPoint2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetCutPoint2` método establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte. Este método es equivalente a [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md), pero toma un valor [**REFTIME**](reftime.md) .

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

Punto de corte relativo al inicio de la transición, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

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

[**Interfaz IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




