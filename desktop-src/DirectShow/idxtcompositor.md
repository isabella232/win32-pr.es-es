---
description: La interfaz IDxtCompositor establece las propiedades en la transición de Compositor. Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de Compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaz IDxtCompositor (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973768"
---
# <a name="idxtcompositor-interface"></a>Interfaz IDxtCompositor

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

La `IDxtCompositor` interfaz establece las propiedades en la transición de [Compositor.](compositor-transition.md)

Esta interfaz la usa internamente DirectShow Editing Services (DES) cuando representa la transición de Compositor. Las aplicaciones DES no tienen que usar esta interfaz. Para establecer las propiedades en una transición en DES, use la [**interfaz IPropertySetter.**](ipropertysetter.md)

La transición compositora compone una imagen de primer plano en una imagen de fondo. El *rectángulo de origen* define la sección de la imagen de primer plano que se compone. El *rectángulo de destino* define la sección de la imagen de fondo que recibe la imagen de primer plano. En el diagrama siguiente se muestran estos rectángulos.

![propiedades de transición de compositor](images/compmeasure.png)

## <a name="members"></a>Members

La **interfaz IDxtCompositor** hereda de **IDXEffect.** **IDxtCompositor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDxtCompositor** tiene estos métodos.



| Método                                                   | Descripción                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**get \_ Height**](idxtcompositor-get-height.md)         | Recupera el alto del rectángulo de destino.<br/>            |
| [**get \_ OffsetX**](idxtcompositor-get-offsetx.md)       | Recupera el desplazamiento horizontal del rectángulo de destino.<br/> |
| [**get \_ OffsetY**](idxtcompositor-get-offsety.md)       | Recupera el desplazamiento vertical del rectángulo de destino.<br/>   |
| [**get \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera el alto del rectángulo de origen.<br/>            |
| [**get \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera el desplazamiento horizontal del rectángulo de origen.<br/> |
| [**get \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera el desplazamiento vertical del rectángulo de origen.<br/>   |
| [**get \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera el ancho del rectángulo de origen.<br/>             |
| [**get \_ Width**](idxtcompositor-get-width.md)           | Recupera el ancho del rectángulo de destino.<br/>             |
| [**put \_ Height**](idxtcompositor-put-height.md)         | Especifica el alto del rectángulo de destino.<br/>            |
| [**put \_ OffsetX**](idxtcompositor-put-offsetx.md)       | Especifica el desplazamiento horizontal del rectángulo de destino.<br/> |
| [**put \_ OffsetY**](idxtcompositor-put-offsety.md)       | Especifica el desplazamiento vertical del rectángulo de destino.<br/>   |
| [**put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Especifica el alto del rectángulo de origen.<br/>            |
| [**put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Especifica el desplazamiento horizontal del rectángulo de origen.<br/> |
| [**put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Especifica el desplazamiento vertical del rectángulo de origen.<br/>   |
| [**put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Especifica el ancho del rectángulo de origen.<br/>             |
| [**put \_ Width**](idxtcompositor-put-width.md)           | Especifica el ancho del rectángulo de destino.<br/>             |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




