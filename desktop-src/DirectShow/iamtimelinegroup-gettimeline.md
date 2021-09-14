---
description: El método GetTimeline recupera la escala de tiempo a la que pertenece este grupo.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: Método IAMTimelineGroup::GetTimeline (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b85b0c6f1730c2946134a36d33537f311b6603f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886985"
---
# <a name="iamtimelinegroupgettimeline-method"></a>IAMTimelineGroup::GetTimeline (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetTimeline` método recupera la escala de tiempo a la que pertenece este grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTimeline* \[ out\]
</dt> <dd>

Recibe la interfaz [**IAMTimeline**](iamtimeline.md) de la escala de tiempo. Si el grupo no forma parte de una escala de tiempo, el valor se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si el valor devuelto en *ppTimeline* no es **NULL,** la **interfaz IAMTimeline** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




