---
description: El método GetCutPoint recupera el punto de corte.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'IAMTimelineTrans:: GetCutPoint (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691027"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>IAMTimelineTrans:: GetCutPoint (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetCutPoint` método recupera el punto de corte. Si representa una transición como un corte, el punto de corte es el momento en que la transición corta de un origen al siguiente. De forma predeterminada, este valor es el medio de la transición. Por ejemplo, en una transición que abarca un segundo, el punto de corte predeterminado es de 0,5 segundos en la transición.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTLTime* 
</dt> <dd>

Recibe el punto de corte, relativo a la hora de inicio de la transición, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                               | Descripción                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | No se estableció el punto de corte. El valor devuelto es el valor predeterminado.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El punto de corte se estableció en un valor distinto del predeterminado.<br/>            |
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo** .<br/>                                          |



 

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

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutsOnly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




