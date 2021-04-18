---
description: La interfaz IRenderEngine2 permite que la aplicación Reemplace el filtro de cambio de tamaño de vídeo predeterminado utilizado por los servicios de edición de DirectShow (DES). El motor de representación básico y el motor de representación inteligente admiten esta interfaz.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaz IRenderEngine2 (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681025"
---
# <a name="irenderengine2-interface"></a>Interfaz IRenderEngine2

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IRenderEngine2` interfaz permite que la aplicación Reemplace el filtro de cambio de tamaño de vídeo predeterminado utilizado por los servicios de edición de DirectShow (des). El [motor de representación básico](basic-render-engine.md) y el [motor de representación inteligente](smart-render-engine.md) admiten esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IRenderEngine2** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IRenderEngine2** tiene estos métodos.



| Método                                                  | Descripción                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Especifica el CLSID de un filtro de cambio de tamaño personalizado proporcionado por la aplicación.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9,0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Proporcionar un tamaño de vídeo personalizado](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
