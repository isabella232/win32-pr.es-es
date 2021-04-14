---
title: FMA (Corecrt \_ Math. h)
description: Devuelve la suma de multiplicación con fusibles de doble precisión de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- HLSL de FMA
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422288"
---
# <a name="fma"></a>fma

Devuelve la suma de multiplicación con fusibles de doble precisión de \* b + c.



| *RET* FMA (doble *a*, *b*, *c*); |
|----------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="a"></span><span id="A"></span>*un*
</dt> <dd>

\[en \] el primer valor de la suma de multiplicación fusionada.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[en \] el segundo valor de la suma de multiplicación fusionada.

</dd> <dt>

<span id="c"></span><span id="C"></span>*unidad*
</dt> <dd>

\[en \] el tercer valor de la suma de multiplicación fusionada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Multiplicación de doble precisión fusionada de los parámetros *a* \* *b*  +  *c*. El valor devuelto debe ser preciso para 0,5 unidades de menos precisión (ULP).

## <a name="remarks"></a>Observaciones

El intrínseco de **FMA** debe admitir Nan, INF y desnormativas.

Para usar la función intrínseca de **FMA** en el código del sombreador, llame al método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones de D3D11 D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para comprobar que el dispositivo Direct3D admite la opción de característica [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . El intrínseco de **FMA** requiere un controlador de pantalla WDDM 1,2, y todos los controladores de pantalla WDDM 1,2 deben ser compatibles con **FMA**. Si la aplicación crea un dispositivo de representación con el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 y el destino de compilación es Shader Model 5 o posterior, el código fuente HLSL puede usar la función intrínseca de **FMA** .

### <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamaño                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *un*   | [**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vector** o **matriz** | [**double**](/windows/desktop/WinProg/windows-data-types)                       | cualquiera                          |
| *b*   | igual que *la entrada a*                                                                                              | [**double**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que *la entrada a* |
| *c*   | igual que *la entrada a*                                                                                              | [**double**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que *la entrada a* |
| *direcc* | igual que *la entrada a*                                                                                              | [**double**](/windows/desktop/WinProg/windows-data-types)                       | las mismas dimensiones que *la entrada a* |



 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                | Compatible |
|-------------------------------------------------------------|-----------|
| [Modelo de sombreador 5 o posterior](d3d11-graphics-reference-sm5.md) | sí       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                          |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

