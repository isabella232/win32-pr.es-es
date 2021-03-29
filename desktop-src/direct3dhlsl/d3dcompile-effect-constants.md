---
title: Constantes de D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Estas constantes dirigen el modo en que el compilador compila un archivo de efectos o el modo en que el tiempo de ejecución procesa el archivo de efecto.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986796"
---
# <a name="d3dcompile_effect-constants"></a>Constantes de efecto de D3DCOMPILE \_

Estas constantes dirigen el modo en que el compilador compila un archivo de efectos o el modo en que el tiempo de ejecución procesa el archivo de efecto.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Efecto secundario del efecto de D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compilar el archivo de efectos (. FX) en un efecto secundario. Los efectos secundarios no tienen inicializadores para los valores compartidos porque estos efectos secundarios se inicializan en el efecto maestro (el grupo de efectos).

> [!Note]  
> Los grupos de efectos son compatibles con los efectos 10 (FX10), pero no con los efectos 11 (FX11). Para obtener más información sobre las diferencias entre los grupos de efectos de Direct3D 10 y los grupos de efectos en Direct3D 11, consulte grupos de [efectos y grupos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ efecto \_ permitir \_ operaciones lentas \_**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Deshabilita el modo de rendimiento y permite objetos de estado mutables.

De forma predeterminada, el modo de rendimiento está habilitado. El modo de rendimiento no permite objetos de estado mutable impidiendo que las expresiones no literales aparezcan en las definiciones de objeto de estado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

