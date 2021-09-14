---
description: La interfaz IAMTimelineTrans proporciona métodos para manipular transiciones en DirectShow Editing Services (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interfaz IAMTimelineTrans (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072194"
---
# <a name="iamtimelinetrans-interface"></a>Interfaz IAMTimelineTrans

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IAMTimelineTrans` interfaz proporciona métodos para manipular transiciones [en DirectShow Editing Services](directshow-editing-services.md) (DES). Una transición es una progresión entre una capa de vídeo y la composición representado de todas las capas de vídeo con una prioridad inferior. Se puede agregar una transición a cualquier objeto de escala de tiempo que exponga la [**interfaz IAMTimelineTransable.**](iamtimelinetransable.md) Para establecer propiedades en una transición, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

El objeto de transición DES es realmente un contenedor para un objeto de transformación de DirectX. Cualquier objeto directX Transform de 2 entradas se puede usar para implementar el efecto visual para la transición. Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros. Para especificar el objeto DirectX Transform para una transición, llame al [**método IAMTimelineObj::SetSubObjectGUID.**](iamtimelineobj-setsubobjectguid.md)

Para crear un objeto de transición, llame a [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor TIMELINE \_ MAJOR TYPE \_ \_ TRANSITION. Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineTrans` interfaz .

## <a name="members"></a>Members

La **interfaz IAMTimelineTrans** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrans** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IAMTimelineTrans** tiene estos métodos.



| Método                                                  | Descripción                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | Recupera el punto de corte.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Recupera el punto de corte, como un [**valor REFTIME.**](reftime.md)<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | Determina si la transición se representa como un corte.<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | Recupera un valor que indica si se intercambian las entradas de transición.<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | Establece el punto de corte.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Establece el punto de corte, como un [**valor REFTIME.**](reftime.md)<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | Especifica si la transición se representa como un corte.<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | Especifica si se intercambian las entradas de transición.<br/>                        |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Trabajar con efectos y transiciones](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
