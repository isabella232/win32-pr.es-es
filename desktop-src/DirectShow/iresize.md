---
description: La interfaz IResize debe ser compatible con cualquier filtro personalizado de cambio de tamaño de vídeo DirectShow Editing Services (DES). Para establecer un filtro de cambio de tamaño personalizado, llame al método IRenderEngine2::SetResizerGUID en el motor de representación.
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaz IResize (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 19aabd7c04cb5350ef3da87e1a20db6b75f6546f0fbcf5af3422c152bcafcf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818074"
---
# <a name="iresize-interface"></a>Interfaz IResize

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La interfaz debe ser compatible con cualquier filtro personalizado de cambio de tamaño de `IResize` vídeo DirectShow Editing Services (DES). Para establecer un filtro de cambio de tamaño personalizado, llame al método [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) en el motor de representación.

## <a name="members"></a>Miembros

La **interfaz IResize** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IResize** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IResize** tiene estos métodos.



| Método                                          | Descripción                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**get \_ InputSize**](iresize-get-inputsize.md) | Devuelve el tamaño de entrada actual del filtro de cambio de tamaño.<br/>  |
| [**get \_ MediaType**](iresize-get-mediatype.md) | Devuelve el tipo de medio de salida del filtro de cambio de tamaño.<br/>   |
| [**get \_ Size**](iresize-get-size.md)           | Devuelve el tamaño de salida actual y el modo de ajuste.<br/> |
| [**put \_ MediaType**](iresize-put-mediatype.md) | Establece el tipo de medio de salida.<br/>                       |
| [**put \_ Size**](iresize-put-size.md)           | Establece el tamaño de salida y el modo de ajuste.<br/>            |



 

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

 

 
