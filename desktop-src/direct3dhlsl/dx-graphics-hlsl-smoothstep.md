---
title: smoothstep
description: Devuelve una interpolación hermite suave entre 0 y 1, si x está en el intervalo \ min, max\ .
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974706"
---
# <a name="smoothstep"></a>smoothstep

Devuelve una interpolación hermite suave entre 0 y 1, si *x* está en el intervalo \[ *mínimo*, *máx.* \]



| *ret* smoothstep(*min*, *max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parámetros



| Elemento                                                         | Descripción                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*Min*<br/> | \[en \] El intervalo mínimo del parámetro *x.*<br/> |
| <span id="max"></span><span id="MAX"></span>*máximo*<br/> | \[en \] El intervalo máximo del parámetro *x.*<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[en \] El valor especificado que se va a interpolar.<br/> |



 

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si *x* es menor que *min*; 1 si *x* es mayor que *max*; de lo contrario, un valor entre 0 y 1 si *x* está en el intervalo \[ *mínimo*, *máx.* \]

## <a name="remarks"></a>Observaciones

Use la función intrínseca HLSL **smoothstep** para crear una transición sin problemas entre dos valores. Por ejemplo, puede usar esta función para combinar dos colores sin problemas.

## <a name="type-description"></a>Descripción del tipo



| Nombre  | [**Tipo de plantilla**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**escalar,**](dx-graphics-hlsl-intrinsic-functions.md) **vector** o **matriz** | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | cualquiera                            |
| *min* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *max* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |
| *Ret* | igual que la entrada *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | las mismas dimensiones que la entrada *x* |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                                                       | Compatible           |
|------------------------------------------------------------------------------------|---------------------|
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) y modelos de sombreador superiores | sí                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | sí (solo \_ frente a \_ 1 1) |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Funciones intrínsecas (HLSL de DirectX)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

