---
description: La interfaz IDxtCompositor establece propiedades en la transición del compositor. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición del compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaz IDxtCompositor (QEDIT. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680900"
---
# <a name="idxtcompositor-interface"></a>Interfaz IDxtCompositor

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IDxtCompositor` interfaz establece las propiedades en la transición del [compositor](compositor-transition.md) .

Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición del compositor. Las aplicaciones DES no tienen que usar esta interfaz. Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .

La transición de compositor compone una imagen de primer plano en una imagen de fondo. El *rectángulo de origen* define la sección de la imagen de primer plano que se compone. El *rectángulo de destino* define la sección de la imagen de fondo que recibe la imagen de primer plano. En el siguiente diagrama se ilustran estos rectángulos.

![propiedades de la transición de compositor](images/compmeasure.png)

## <a name="members"></a>Miembros

La interfaz **IDxtCompositor** hereda de **IDXEffect**. **IDxtCompositor** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDxtCompositor** tiene estos métodos.



| Método                                                   | Descripción                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [**obtener \_ alto**](idxtcompositor-get-height.md)         | Recupera el alto del rectángulo de destino.<br/>            |
| [**obtener \_ offsetX**](idxtcompositor-get-offsetx.md)       | Recupera el desplazamiento horizontal del rectángulo de destino.<br/> |
| [**obtener \_ desplazamiento**](idxtcompositor-get-offsety.md)       | Recupera el desplazamiento vertical del rectángulo de destino.<br/>   |
| [**obtener \_ SrcHeight**](idxtcompositor-get-srcheight.md)   | Recupera el alto del rectángulo de origen.<br/>            |
| [**obtener \_ SrcOffsetX**](idxtcompositor-get-srcoffsetx.md) | Recupera el desplazamiento horizontal del rectángulo de origen.<br/> |
| [**obtener \_ SrcOffsetY**](idxtcompositor-get-srcoffsety.md) | Recupera el desplazamiento vertical del rectángulo de origen.<br/>   |
| [**obtener \_ SrcWidth**](idxtcompositor-get-srcwidth.md)     | Recupera el ancho del rectángulo de origen.<br/>             |
| [**obtener \_ ancho**](idxtcompositor-get-width.md)           | Recupera el ancho del rectángulo de destino.<br/>             |
| [**colocar \_ alto**](idxtcompositor-put-height.md)         | Especifica el alto del rectángulo de destino.<br/>            |
| [**Put \_ offsetX**](idxtcompositor-put-offsetx.md)       | Especifica el desplazamiento horizontal del rectángulo de destino.<br/> |
| [**colocar \_ desplazamiento**](idxtcompositor-put-offsety.md)       | Especifica el desplazamiento vertical del rectángulo de destino.<br/>   |
| [**Put \_ SrcHeight**](idxtcompositor-put-srcheight.md)   | Especifica el alto del rectángulo de origen.<br/>            |
| [**Put \_ SrcOffsetX**](idxtcompositor-put-srcoffsetx.md) | Especifica el desplazamiento horizontal del rectángulo de origen.<br/> |
| [**Put \_ SrcOffsetY**](idxtcompositor-put-srcoffsety.md) | Especifica el desplazamiento vertical del rectángulo de origen.<br/>   |
| [**Put \_ SrcWidth**](idxtcompositor-put-srcwidth.md)     | Especifica el ancho del rectángulo de origen.<br/>             |
| [**colocar \_ ancho**](idxtcompositor-put-width.md)           | Especifica el ancho del rectángulo de destino.<br/>             |



 

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



 

 




