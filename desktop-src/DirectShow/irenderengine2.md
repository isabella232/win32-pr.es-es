---
description: La interfaz IRenderEngine2 permite a la aplicación reemplazar el filtro de tamaño de vídeo predeterminado que usa DirectShow Editing Services (DES). El motor de representación básico y el motor de representación inteligente admiten esta interfaz.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaz IRenderEngine2 (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891793"
---
# <a name="irenderengine2-interface"></a>Interfaz IRenderEngine2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz permite a la aplicación reemplazar el filtro de tamaño de vídeo predeterminado usado `IRenderEngine2` por DirectShow Editing Services (DES). El [motor de representación básico y](basic-render-engine.md) el motor de representación [inteligente](smart-render-engine.md) admiten esta interfaz.

## <a name="members"></a>Members

La **interfaz IRenderEngine2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRenderEngine2** tiene estos métodos.



| Método                                                  | Descripción                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Especifica el CLSID de un filtro de tamaño personalizado proporcionado por la aplicación.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Proporcionar un cambio de tamaño de vídeo personalizado](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
