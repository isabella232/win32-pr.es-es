---
description: La interfaz IAMTimelineEffect proporciona métodos para manipular efectos de audio y vídeo en DirectShow Editing Services (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaz IAMTimelineEffect (Qedit.h)
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
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052765"
---
# <a name="iamtimelineeffect-interface"></a>IamTimelineEffect (interfaz)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineEffect` interfaz proporciona métodos para manipular efectos de audio y vídeo [en DirectShow Editing Services](directshow-editing-services.md) (DES). Se puede agregar un efecto a cualquier objeto de escala de tiempo que exponga la [**interfaz IAMTimelineEffectable.**](iamtimelineeffectable.md) Para establecer propiedades en un efecto, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

El objeto de efecto DES es realmente un contenedor para uno de los otros dos objetos:

-   En el caso de los efectos de audio, DirectShow filtro de efecto de audio.
-   Para efectos de vídeo y objeto de transformación de DirectX de 1 entrada.

Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros.

Para especificar el filtro o el objeto Transform de DirectX para un efecto, llame al [**método IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Para crear un objeto de efecto, llame a [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ EFFECT. Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineEffect` interfaz .

## <a name="members"></a>Miembros

La **interfaz IAMTimelineEffect** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineEffect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineEffect** tiene estos métodos.



| Método                                                           | Descripción                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Recupera el nivel de prioridad del efecto.<br/> |



 

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

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
