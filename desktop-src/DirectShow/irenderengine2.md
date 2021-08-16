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
ms.openlocfilehash: 39f1bc68fc6cd76e87d1998047cb211b3a8aa8e263c90e0494c7eaf15d52f75f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818513"
---
# <a name="irenderengine2-interface"></a>Interfaz IRenderEngine2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz permite a la aplicación reemplazar el filtro de tamaño de vídeo predeterminado que `IRenderEngine2` usa DirectShow Editing Services (DES). El [motor de representación básico y](basic-render-engine.md) el motor de representación [inteligente](smart-render-engine.md) admiten esta interfaz.

## <a name="members"></a>Miembros

La **interfaz IRenderEngine2** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IRenderEngine2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRenderEngine2** tiene estos métodos.



| Método                                                  | Descripción                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Especifica el CLSID de un filtro de tamaño personalizado proporcionado por la aplicación.<br/> |



 

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Proporcionar un cambio de tamaño de vídeo personalizado](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
