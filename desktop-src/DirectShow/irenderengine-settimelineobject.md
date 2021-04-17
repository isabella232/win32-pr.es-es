---
description: El método SetTimelineObject establece la escala de tiempo para que la use el motor de representación.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine:: SetTimelineObject (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680708"
---
# <a name="irenderenginesettimelineobject-method"></a>IRenderEngine:: SetTimelineObject (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetTimelineObject` método establece la escala de tiempo para que la use el motor de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntero a la interfaz [**IAMTimeline**](iamtimeline.md) del objeto Timeline.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Memoria insuficiente.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>              | Puntero no válido.<br/>                    |



 

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

[**Interfaz IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




