---
title: Método IDWriteFactory2 CreateCustomRenderingParams
description: Crea un objeto de parámetros de representación con las propiedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Método CreateCustomRenderingParams direct write
- Método CreateCustomRenderingParams direct write , interfaz IDWriteFactory2
- Método CreateCustomRenderingParams de la interfaz IDWriteFactory2
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e85057c28e1ad969fe72711c86aab9657126c760ea3041a08bc5101877686a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071699"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>Método IDWriteFactory2::CreateCustomRenderingParams

Crea un objeto de parámetros de representación con las propiedades especificadas.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Gamma* 
</dt> <dd>

Tipo: **FLOAT**

Valor gamma usado para la corrección gamma, que debe ser mayor que cero y no puede superar 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

La cantidad de mejora de contraste, cero o mayor.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **FLOAT**

La cantidad de mejora de contraste, cero o mayor.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **FLOAT**

El grado de nivel ClearType, de 0,0f (sin ClearType) a 1,0f (ClearType completo).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **DWRITE \_ PIXEL \_ GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Geometría de un píxel de dispositivo.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ RENDERING \_ MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Método de representación de glifos. En la mayoría de los casos, debe ser DWRITE \_ RENDERING MODE DEFAULT para usar automáticamente un modo \_ \_ adecuado.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Cómo ajustar a la cuadrícula los contornos de glifo. En la mayoría de los casos, debe ser DWRITE \_ GRID FIT DEFAULT para elegir automáticamente un modo \_ \_ adecuado.

</dd> <dt>

*renderingParams* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Contiene el objeto de parámetros de representación recién creado o NULL en caso de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

