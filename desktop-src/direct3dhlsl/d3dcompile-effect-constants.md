---
title: D3DCOMPILE_EFFECT constantes (D3DCompiler.h)
description: Estas constantes dirigen cómo el compilador compila un archivo de efecto o cómo el tiempo de ejecución procesa el archivo de efecto.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264324"
---
# <a name="d3dcompile_effect-constants"></a>Constantes D3DCOMPILE \_ EFFECT

Estas constantes dirigen cómo el compilador compila un archivo de efecto o cómo el tiempo de ejecución procesa el archivo de efecto.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**EFECTO SECUNDARIO D3DCOMPILE \_ \_ \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compile el archivo de efectos (.fx) en un efecto secundario. Los efectos secundarios no tienen inicializadores para ningún valor compartido porque estos efectos secundarios se inicializan en el efecto maestro (el grupo de efectos).

> [!Note]  
> Los grupos de efectos son compatibles con Effects 10 (FX10), pero no con Effects 11 (FX11). Para obtener más información sobre las diferencias entre los grupos de efectos en Direct3D 10 y los grupos de efectos en Direct3D 11, vea [Grupos de efectos y grupos.](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**EFECTO D3DCOMPILE \_ PERMITIR \_ OPERACIONES \_ \_ LENTAS**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Deshabilita el modo de rendimiento y permite objetos de estado mutable.

De forma predeterminada, el modo de rendimiento está habilitado. El modo de rendimiento no permite objetos de estado mutable al impedir que las expresiones no literales aparezcan en las definiciones de objetos de estado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DCompiler.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

