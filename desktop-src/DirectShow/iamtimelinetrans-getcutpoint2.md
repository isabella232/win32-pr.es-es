---
description: 'El método GetCutPoint2 recupera el punto de corte. Este método es equivalente a IAMTimelineTrans:: GetCutPoint, pero toma un valor REFTIME.'
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'IAMTimelineTrans:: GetCutPoint2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691026"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a>IAMTimelineTrans:: GetCutPoint2 (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetCutPoint2` método recupera el punto de corte. Este método es equivalente a [**IAMTimelineTrans:: GetCutPoint**](iamtimelinetrans-getcutpoint.md), pero toma un valor [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTLTime* 
</dt> <dd>

Recibe el punto de corte, en segundos, con respecto a la hora de inicio de la transición.

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

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




