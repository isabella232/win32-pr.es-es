---
description: El método GetDuration2 recupera la duración de la escala de tiempo. Este método es equivalente a IAMTimeline::GetDuration, pero toma un parámetro de tipo double.
ms.assetid: 49f5eed3-7fab-4f08-b65c-300349b197cb
title: Método IAMTimeline::GetDuration2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDuration2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc840e642f6c08825f6f53869229e9cc27e87b38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160169"
---
# <a name="iamtimelinegetduration2-method"></a>IamTimeline::GetDuration2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetDuration2` método recupera la duración de la escala de tiempo. Este método es equivalente a [**IAMTimeline::GetDuration**](iamtimeline-getduration.md), pero toma un parámetro de tipo **double**.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDuration2(
   double *pDuration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDuration* 
</dt> <dd>

Recibe la duración de la escala de tiempo, en fracciones de segundo.

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

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




