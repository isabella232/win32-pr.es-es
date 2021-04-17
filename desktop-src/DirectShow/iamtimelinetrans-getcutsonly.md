---
description: El método GetCutsOnly determina si la transición se representa como un corte. Si es así, la transición se produce de forma instantánea en el punto de corte.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: 'IAMTimelineTrans:: GetCutsOnly (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d3bbec55ddfe77c053135054fde9b64efce516a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691025"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>IAMTimelineTrans:: GetCutsOnly (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetCutsOnly` método determina si la transición se representa como un corte. Si es así, la transición se produce de forma instantánea en el punto de corte.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCutsOnly(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe un valor booleano que especifica si la transición se representa como un corte. Si es **true**, la transición es un corte instantáneo. Si **es false**, la transición se produce a lo largo de su duración normal.

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

[**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




