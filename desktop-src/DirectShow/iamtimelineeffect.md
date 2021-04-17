---
description: La interfaz IAMTimelineEffect proporciona métodos para manipular los efectos de audio y vídeo en los servicios de edición de DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaz IAMTimelineEffect (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681256"
---
# <a name="iamtimelineeffect-interface"></a>Interfaz IAMTimelineEffect

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IAMTimelineEffect` interfaz proporciona métodos para manipular los efectos de audio y vídeo en los [servicios de edición de DirectShow](directshow-editing-services.md) (des). Se puede Agregar un efecto a cualquier objeto Timeline que exponga la interfaz [**IAMTimelineEffectable**](iamtimelineeffectable.md) . Para establecer las propiedades de un efecto, use la interfaz [**IPropertySetter**](ipropertysetter.md) .

El objeto de efecto DES es realmente un contenedor para uno de otros dos objetos:

-   Para los efectos de audio, cualquier filtro de efecto de audio de DirectShow.
-   En el caso de efectos de vídeo y 1-entrada de objeto de transformación de DirectX.

Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros.

Para especificar el filtro o el objeto de transformación de DirectX para un efecto, llame al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Para crear un objeto de efecto, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el \_ efecto de tipo principal de la escala de tiempo \_ \_ . Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineEffect` interfaz.

## <a name="members"></a>Miembros

La interfaz **IAMTimelineEffect** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAMTimelineEffect** tiene estos métodos.



| Método                                                           | Descripción                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Recupera el nivel de prioridad del efecto.<br/> |



 

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

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
