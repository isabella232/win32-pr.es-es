---
description: Las directivas del compilador optimizan la funcionalidad que usa la biblioteca DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Directivas del compilador de directXMath Library
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361551"
---
# <a name="directxmath-library-compiler-directives"></a>Directivas del compilador de directXMath Library

Las directivas del compilador optimizan la funcionalidad que usa la biblioteca DirectXMath.



| Directiva                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ NO \_ INTRINSICS\_        | Cuando \_ se define XM NO INTRINSICS, las operaciones \_ directXMath se implementan sin usar intrínsecos \_ \_ específicos de la plataforma. En su lugar, DirectXMath solo usa operaciones de punto flotante estándar.<br/> De forma predeterminada, \_ \_ XM NO \_ INTRINSICS no está \_ definido.<br/> Esta directiva invalida todas las demás directivas. Por lo tanto, se recomienda comprobar XM NO INTRINSICS antes de determinar el estado de INTRÍNSECOS DE XM ARM NEON o \_ \_ \_ XM \_ \_ \_ \_ \_ \_ \_ \_ SSE \_ INTRINSICS \_ .<br/>                                                                              |
| \_\_INTRÍNSECOS DE XM SSE \_\_       | Cuando \_ se define XM SSE INTRINSICS, el código se compila para usar SSE y \_ \_ SSE2 compatibles en plataformas que admiten \_ estos conjuntos de instrucciones.<br/> Las Windows que proporcionan intrínsecos SSE admiten SSE y SSE2.<br/> \_XM \_ SSE \_ INTRINSICS \_ no tiene ningún efecto en los sistemas que no admiten SSE y SSE2.<br/> De forma predeterminada, \_ XM \_ SSE \_ INTRINSICS \_ se define cuando los usuarios compilan para Windows plataforma.<br/> DirectXMath usa el compilador estándar define \_ (M \_ IX86 /M AMD64) para determinar Windows \_ x86 o Windows \_ destinos x64.<br/> |
| \_INTRÍNSECOS DE XM \_ ARM \_ NEON \_\_ | Esto indica los usos de implementación de DirectXMath de los intrínsecos ARM-NEON. De forma predeterminada, XM ARM NEON INTRINSICS se define cuando los usuarios compilan \_ \_ para Windows plataforma \_ \_ \_ ARM/ARM64. DirectXMath usa la definición del compilador estándar \_ (M \_ ARM, \_ M \_ ARM64) para determinar este destino binario.<br/> La compatibilidad con intrínsecos ARM-NEON es nueva en DirectXMath y XNAMath 2.x no la admite.<br/>                                                                                                                                                                             |
| \_\_INTRÍNSECOS DE XM SSE3 \_\_      | Novedad de DirectXMath 3.10. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos de SSE3 cuando proceda; de lo contrario, usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_\_INTRÍNSECOS DE XM SSE4 \_\_      | Novedad de DirectMath 3.09. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3 y SSE4.1 cuando proceda; de lo contrario, usa SSE/SSE2. Cuando se especifica esta directiva de compilador, también implica \_ XM \_ SSE3 \_ INTRINSICS \_ y XM \_ \_ SSE \_ INTRINSICS \_ .<br/>                                                                                                                                                                                                                                |
| \_\_INTRÍNSECOS DE XM AVX \_\_       | Novedad de DirectXMath 3.09. <br/> El uso de /arch:AVX habilitará esta directiva. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para usar intrínsecos de SSE3, SSE4.1 y AVX de 128 bits, si procede; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se especifica esta directiva de compilador, también implica \_ XM \_ SSE3 \_ INTRINSICS, \_ XM \_ SSE4 INTRINSICS y \_ XM SSE INTRINSICS, e \_ \_ \_ \_ incluye \_ un pequeño subconjunto de instrucciones SSE3. <br/>                                                                    |
| INTRÍNSECOS DE XM \_ AVX2 \_\_        | Novedad de DirectXMath 3.11. <br/> El uso de /arch:AVX2 habilita esta directiva. Cuando se especifica esta directiva de compilador, las funciones de DirectXMath usan los intrínsecos AVX2, F16C/CVT16, FMA3, AVX de 128 bits, SSE4.1 y SSE3 cuando proceda. Cuando se usan INTRÍNSECOS DE XM AVX2, implica LOS INTRÍNSECOS \_ \_ DE XM \_ \_ \_ \_ F16C, LOS \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTRÍNSECOS DE \_ XM FMA3, LOS INTRÍNSECOS DE XM AVX, LOS INTRÍNSECOS DE XM SSE3 y los INTRÍNSECOS de XM SSE4.<br/>                                                                                       |
| \_XM \_ F16C \_ INTRINSICS\_      | Novedad de DirectXMath 3.09. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3, SSE4.1, AVX de 128 bits y F16C/CVT16, si procede; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se usan INTRÍNSECOS F16C de XM, implica INTRÍNSECOS DE XM AVX, INTRÍNSECOS de XM SSE, INTRÍNSECOS de XM SSE3 y INTRÍNSECOS \_ \_ de \_ \_ \_ \_ \_ XM \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SSE4. \_ \_<br/>                                                                                                                                                 |
| \_\_INTRÍNSECOS FMA3 DE XM \_\_      | Novedad de DirectXMath 3.11. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath usarán los intrínsecos SSE3, SSE4.1, AVX de 128 bits y FMA3 cuando proceda; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se usan INTRÍNSECOS FMA3 de XM, implica INTRÍNSECOS DE XM AVX, INTRÍNSECOS de XM SSE, INTRÍNSECOS de XM SSE3 y INTRÍNSECOS \_ \_ de \_ \_ \_ \_ \_ XM \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SSE4. \_ \_ <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Esto permite el uso de la convención de llamada \_ \_ vectorcall Windows destinos x86 Windows x64. El valor predeterminado es \_ XM \_ VECTORCALL \_ =1 cuando el compilador admite esta característica. Puede establecerlo manualmente en \_ XM \_ VECTORCALL \_ =0 para deshabilitarlo siempre. <br/> \_\_Vectorcall no se admite para la Windows plataforma ARM/ARM64 o C++ administrado. <br/>                                                                                                                                                                                                                 |
| \_\_INTRÍNSECOS DE XM SVML \_\_     | Novedad de DirectXMath 3.16. <br/> Con VS 2019 o versiones posteriores, esto permite a la biblioteca usar la Biblioteca de matriz de vectores cortos de Intel para &reg; x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
