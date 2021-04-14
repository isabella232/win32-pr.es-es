---
title: IDWriteFactory2 CreateCustomRenderingParams, método
description: Crea un objeto de parámetros de representación con las propiedades especificadas.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Método CreateCustomRenderingParams de escritura directa
- Método CreateCustomRenderingParams de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método CreateCustomRenderingParams
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
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422448"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a>IDWriteFactory2:: CreateCustomRenderingParams (método)

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

*gamma* 
</dt> <dd>

Tipo: **float**

El valor gamma utilizado para la corrección gamma, que debe ser mayor que cero y no puede superar 256.

</dd> <dt>

*enhancedContrast* 
</dt> <dd>

Tipo: **float**

La cantidad de mejoras de contraste, cero o más.

</dd> <dt>

*grayscaleEnhancedContrast* 
</dt> <dd>

Tipo: **float**

La cantidad de mejoras de contraste, cero o más.

</dd> <dt>

*clearTypeLevel* 
</dt> <dd>

Tipo: **float**

El grado de nivel de ClearType, de 0,0 f (sin ClearType) a 1,0 f (completo ClearType).

</dd> <dt>

*pixelGeometry* 
</dt> <dd>

Tipo: **[ **DWRITE \_ píxel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**

Geometría de un píxel de dispositivo.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **[ **\_ \_ modo de representación DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**

Método de representación de glifos. En la mayoría de los casos, debe ser el \_ \_ modo de representación DWRITE \_ predeterminado para usar automáticamente un modo adecuado.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ \_ \_ modo de ajuste de cuadrícula**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Cómo ajustar la cuadrícula a los contornos del glifo. En la mayoría de los casos, debe ser DWRITE \_ cuadrícula de \_ ajuste \_ predeterminada para elegir automáticamente un modo adecuado.

</dd> <dt>

*renderingParams* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***

Contiene el objeto de parámetros de representación recién creado o NULL en caso de error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

