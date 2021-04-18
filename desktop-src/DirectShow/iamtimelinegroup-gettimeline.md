---
description: El método GetTimeline recupera la escala de tiempo a la que pertenece este grupo.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'IAMTimelineGroup:: GetTimeline (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680305"
---
# <a name="iamtimelinegroupgettimeline-method"></a>IAMTimelineGroup:: GetTimeline (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetTimeline` método recupera la escala de tiempo a la que pertenece este grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTimeline* \[ enuncia\]
</dt> <dd>

Recibe la interfaz [**IAMTimeline**](iamtimeline.md) de la escala de tiempo. Si el grupo no es parte de una escala de tiempo, el valor se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el valor devuelto en *ppTimeline* no es **null**, la interfaz **IAMTimeline** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




