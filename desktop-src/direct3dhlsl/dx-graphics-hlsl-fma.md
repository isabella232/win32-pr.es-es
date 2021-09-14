---
title: fma (Corecrt \_ math.h)
description: Devuelve la multiplicación combinada de precisión doble de \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- fma HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964651"
---
# <a name="fma"></a>fma

Devuelve la suma multiplicada de precisión doble de \* b + c.



| *ret* fma(double *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*Un*
</dt> <dd>

\[en \] El primer valor de la suma multiplicada fusionada.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[en \] El segundo valor de la suma multiplicada.

</dd> <dt>

<span id="c"></span><span id="C"></span>*C*
</dt> <dd>

\[en \] El tercer valor de la suma multiplicada fusionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Suma multiplicada de precisión doble de parámetros *a* \* *b*  +  *c*. El valor devuelto debe ser preciso a 0,5 unidades de precisión mínima (ULP).

## <a name="remarks"></a>Observaciones

El **intrínseco fma** debe admitir NaN, INF y Denorms.

Para usar la función intrínseca **fma** en el código del sombreador, llame al método [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para comprobar que el dispositivo Direct3D admite la opción de característica [**ExtendedDoublesShaderInstructions.**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) El **intrínseco fma** requiere un controlador de pantalla WDDM 1.2 y todos los controladores de pantalla de WDDM 1.2 deben admitir **fma**. Si la aplicación crea un dispositivo de representación con el nivel [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) característica 11.0 o 11.1 y el destino de compilación es el modelo de sombreador 5 o posterior, el código fuente HLSL puede usar la función intrínseca **fma.**

### <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *Un*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**Doble**](/windows/desktop/WinProg/windows-data-types)                       | cualquiera                          |
| *b*   | igual que la entrada *a*                                                                                              | [**Doble**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que la entrada *a* |
| *c*   | igual que la entrada *a*                                                                                              | [**Doble**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que la entrada *a* |
| *Ret* | igual que la entrada *a*                                                                                              | [**Doble**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que la entrada *a* |



 

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                | Compatible |
|-------------------------------------------------------------|-----------|
| [Modelo de sombreador 5 o posterior](d3d11-graphics-reference-sm5.md) | sí       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

