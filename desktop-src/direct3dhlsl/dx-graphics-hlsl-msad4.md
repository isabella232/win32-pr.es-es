---
title: msad4
description: Compara un valor de referencia de 4 bytes y un valor de origen de 8 bytes y acumula un vector de 4 sumas. Cada suma corresponde a la suma enmascarada de diferencias absolutas de una alineación de bytes diferente entre el valor de referencia y el valor de origen.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- HLSL de msad4
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104984143"
---
# <a name="msad4"></a>msad4

Compara un valor de referencia de 4 bytes y un valor de origen de 8 bytes y acumula un vector de 4 sumas. Cada suma corresponde a la suma enmascarada de diferencias absolutas de una alineación de bytes diferente entre el valor de referencia y el valor de origen.



| resultado de uint4 = msad4 (referencia uint, origen uint2, acumulación de uint4); |
|------------------------------------------------------------------|



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="reference"></span><span id="REFERENCE"></span>*referencia*
</dt> <dd>

\[en \] la matriz de referencia de 4 bytes en un valor **uint** .

</dd> <dt>

<span id="source"></span><span id="SOURCE"></span>*fuentes*
</dt> <dd>

\[en \] la matriz de origen de 8 bytes en dos valores de **uint2** .

</dd> <dt>

<span id="accum"></span><span id="ACCUM"></span>*acumulación*
</dt> <dd>

\[en \] un vector de 4 valores. **msad4** agrega este vector a la suma enmascarada de diferencias absolutas de las diferentes alineaciones de bytes entre el valor de referencia y el valor de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vector de 4 sumas. Cada suma corresponde a la suma enmascarada de diferencias absolutas de diferentes alineaciones de bytes entre el valor de referencia y el valor de origen. **msad4** no incluye una diferencia en la suma si esa diferencia se enmascara (es decir, el byte de referencia es 0).

## <a name="remarks"></a>Observaciones

Para usar la función intrínseca **msad4** en el código del sombreador, llame al método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con [**\_ \_ \_ las opciones D3D11 de la característica D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para comprobar que el dispositivo Direct3D admite la opción de la característica [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) . La función intrínseca **msad4** requiere un controlador de pantalla WDDM 1,2 y todos los controladores de pantalla WDDM 1,2 deben admitir **msad4**. Si la aplicación crea un dispositivo de representación con el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 o 11,1 y el destino de compilación es el modelo de sombreador 5 o posterior, el código fuente de HLSL puede usar la función intrínseca **msad4** .

Los valores devueltos solo son precisos hasta 65535. Si llama a la función intrínseca **msad4** con entradas que pueden dar lugar a valores devueltos mayores que 65535, **msad4** produce resultados indefinidos.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                | Compatible |
|-------------------------------------------------------------|-----------|
| [Modelo de sombreador 5 o posterior](d3d11-graphics-reference-sm5.md) | sí       |



 

## <a name="examples"></a>Ejemplos

Este es un ejemplo de cálculo de resultados para **msad4**:


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



Este es un ejemplo de cómo se puede usar **msad4** para buscar un patrón de referencia en un búfer:


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>           |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

