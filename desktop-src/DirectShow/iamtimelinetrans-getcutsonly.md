---
description: El método GetCutsOnly determina si la transición se representa como un corte. Si es así, la transición se produce de forma instantánea en el punto de corte.
ms.assetid: d7959816-1152-4bc4-b3f8-bed69b450530
title: Método IAMTimelineTrans::GetCutsOnly (Qedit.h)
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
ms.openlocfilehash: 7007db4699dc3f1772ad727c2e40daa15946d07d564b92b5b1517899ff6e1f20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154789"
---
# <a name="iamtimelinetransgetcutsonly-method"></a>IamTimelineTrans::GetCutsOnly (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

Recibe un valor booleano que especifica si la transición se representa como un corte. Si **es TRUE,** la transición es un corte instantáneo. Si **es FALSE,** la transición se produce durante su duración normal.

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

[**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




