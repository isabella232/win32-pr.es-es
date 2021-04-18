---
description: 'La interfaz IResize debe ser compatible con cualquier filtro de tamaño de vídeo personalizado para los servicios de edición de DirectShow (DES). Para establecer un filtro de tamaño personalizado, llame al método IRenderEngine2:: SetResizerGUID en el motor de representación.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interfaz IResize (QEDIT. h)
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
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679067"
---
# <a name="iresize-interface"></a>Interfaz IResize

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IResize` interfaz debe ser compatible con cualquier filtro de tamaño de vídeo personalizado para los servicios de edición de DirectShow (des). Para establecer un filtro de tamaño personalizado, llame al método [**IRenderEngine2:: SetResizerGUID**](irenderengine2-setresizerguid.md) en el motor de representación.

## <a name="members"></a>Miembros

La interfaz **IResize** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IResize** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IResize** tiene estos métodos.



| Método                                          | Descripción                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**obtener \_ Input**](iresize-get-inputsize.md) | Devuelve el tamaño de entrada actual del filtro de tamaño.<br/>  |
| [**obtener \_ mediatype**](iresize-get-mediatype.md) | Devuelve el tipo de medio de salida del filtro de tamaño.<br/>   |
| [**obtener \_ tamaño**](iresize-get-size.md)           | Devuelve el tamaño de salida actual y el modo de ajuste.<br/> |
| [**colocar \_ mediatype**](iresize-put-mediatype.md) | Establece el tipo de medio de salida.<br/>                       |
| [**poner \_ tamaño**](iresize-put-size.md)           | Establece el tamaño de salida y el modo de ajuste.<br/>            |



 

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

 

 
