---
description: El método GetTimelineObject recupera la escala de tiempo que el motor de representación está usando actualmente.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: Método IRenderEngine::GetTimelineObject (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062310"
---
# <a name="irenderenginegettimelineobject-method"></a>IRenderEngine::GetTimelineObject (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetTimelineObject` método recupera la escala de tiempo que el motor de representación está usando actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppTimeline* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimeline**](iamtimeline.md) de la escala de tiempo. Recibe el valor **NULL si** no hay ninguna escala de tiempo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>              | Puntero no válido.<br/>                    |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

En la devolución, si el valor de *\* ppTimeline* no es **NULL,** la **interfaz IAMTimeline** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




