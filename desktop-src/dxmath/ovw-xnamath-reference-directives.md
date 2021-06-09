---
description: Las directivas del compilador optimizan la funcionalidad que usa la biblioteca DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Directivas del compilador de directXMath Library
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826780"
---
# <a name="directxmath-library-compiler-directives"></a>Directivas del compilador de directXMath Library

Las directivas del compilador optimizan la funcionalidad que usa la biblioteca DirectXMath.



| Directiva                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ NO \_ INTRINSICS\_        | Cuando se define XM NO INTRINSICS, las operaciones \_ \_ de DirectXMath se implementan sin usar intrínsecos \_ \_ específicos de la plataforma. En su lugar, DirectXMath solo usa operaciones de punto flotante estándar.<br/> De forma predeterminada, \_ NO INTRINSICS de XM \_ no está \_ \_ definido.<br/> Esta directiva invalida todas las demás directivas. Por lo tanto, se recomienda comprobar XM NO INTRINSICS antes de determinar el estado de LOS INTRÍNSECOS DE XM ARM NEON o \_ \_ \_ XM \_ \_ \_ \_ \_ \_ \_ \_ SSE \_ INTRINSICS \_ .<br/>                                                                              |
| \_\_INTRÍNSECOS DE SSE DE XM \_\_       | Cuando \_ se define XM SSE INTRINSICS, el código se compila para usar SSE y SSE2 compatibles en plataformas que \_ \_ \_ admiten estos conjuntos de instrucciones.<br/> Las versiones de Windows que proporcionan funciones intrínsecas de SSE admiten SSE y SSE2.<br/> \_XM \_ SSE \_ INTRINSICS \_ no tiene ningún efecto en los sistemas que no admiten SSE y SSE2.<br/> De forma predeterminada, \_ XM \_ SSE \_ INTRINSICS \_ se define cuando los usuarios compilan para una plataforma Windows.<br/> DirectXMath usa el compilador estándar define \_ (M \_ IX86 /M AMD64) para determinar los destinos \_ x86 o Windows \_ x64.<br/> |
| \_XM \_ ARM \_ NEON \_ INTRINSICS\_ | Esto indica los usos de implementación de DirectXMath de los intrínsecos ARM-NEON. De forma predeterminada, XM ARM NEON INTRINSICS se define cuando los usuarios compilan para \_ Windows en la plataforma \_ \_ \_ \_ ARM/ARM64. DirectXMath usa la definición del compilador estándar \_ (M \_ ARM, \_ M \_ ARM64) para determinar este destino binario.<br/> La compatibilidad con intrínsecos ARM-NEON es nueva en DirectXMath y no es compatible con XNAMath 2.x.<br/>                                                                                                                                                                             |
| \_XM \_ SSE3 \_ INTRINSICS\_      | Novedad de DirectXMath 3.10. <br/> Cuando se especifica esta directiva del compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3, si procede; de lo contrario, usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_XM \_ SSE4 \_ INTRINSICS\_      | Novedad de DirectMath 3.09. <br/> Cuando se especifica esta directiva del compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3 y SSE4.1 cuando proceda; de lo contrario, usa SSE/SSE2. Al especificar esta directiva de compilador, también implica \_ XM \_ SSE3 \_ INTRINSICS \_ y XM \_ \_ SSE \_ INTRINSICS \_ .<br/>                                                                                                                                                                                                                                |
| \_XM \_ AVX \_ INTRINSICS\_       | Novedad de DirectXMath 3.09. <br/> El uso de /arch:AVX habilitará esta directiva. <br/> Cuando se especifica esta directiva del compilador, las funciones de DirectXMath se implementan para usar intrínsecos SSE3, SSE4.1 y AVX de 128 bits, si procede; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se especifica esta directiva de compilador, también implica \_ XM \_ SSE3 \_ INTRINSICS, \_ XM SSE4 INTRINSICS y XM SSE INTRINSICS e incluye un pequeño subconjunto de \_ instrucciones \_ \_ \_ \_ \_ \_ SSE3. <br/>                                                                    |
| XM \_ AVX2 \_ INTRINSICS\_        | Novedad de DirectXMath 3.11. <br/> El uso de /arch:AVX2 habilita esta directiva. Cuando se especifica esta directiva del compilador, las funciones de DirectXMath usan intrínsecos AVX2, F16C/CVT16, FMA3, AVX de 128 bits, SSE4.1 y SSE3 cuando proceda. Cuando se usan INTRÍNSECOS AVX2 de XM, implica INTRÍNSECOS F16C de XM, INTRÍNSECOS FMA3 DE XM, INTRÍNSECOS DE AVX DE XM, INTRÍNSECOS SSE de XM, INTRÍNSECOS SSE3 de XM y INTRÍNSECOS \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ SSE4 de \_ \_ XM.<br/>                                                                                       |
| \_XM \_ F16C \_ INTRINSICS\_      | Novedad de DirectXMath 3.09. <br/> Cuando se especifica esta directiva de compilador, las funciones directXMath se implementan para usar los intrínsecos SSE3, SSE4.1, AVX de 128 bits y F16C/CVT16, si procede; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se usan INTRÍNSECOS F16C de XM, implica INTRÍNSECOS AVX DE XM, INTRÍNSECOS DE SSE de \_ \_ \_ \_ \_ \_ \_ XM, \_ \_ \_ INTRÍNSECOS DE \_ \_ \_ \_ SSE3 \_ \_ \_ \_ \_ \_ de XM y INTRÍNSECOS SSE4 de XM.<br/>                                                                                                                                                 |
| \_\_INTRÍNSECOS FMA3 DE XM \_\_      | Novedad de DirectXMath 3.11. <br/> Cuando se especifica esta directiva del compilador, las funciones de DirectXMath usarán los intrínsecos SSE3, SSE4.1, AVX de 128 bits y FMA3, si procede; De lo contrario, DirectXMath usa SSE/SSE2. Cuando se usan INTRÍNSECOS FMA3 de XM, implica LAS FUNCIONES INTRÍNSECAS DE AVX de XM, LAS INTRÍNSECAS de SSE de XM, LAS INTRÍNSECAS de SSE3 de XM y las \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ INTRÍNSECAS de SSE4 de \_ \_ XM. <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Esto permite el uso de la convención de \_ \_ llamada vectorcall para destinos x86 o Windows x64. El valor predeterminado es \_ XM \_ VECTORCALL \_ =1 cuando el compilador admite esta característica. Puede establecerlo manualmente en \_ XM \_ VECTORCALL \_ =0 para deshabilitarlo siempre. <br/> \_\_Vectorcall no se admite para Windows en la plataforma ARM/ARM64 ni en C++ administrado. <br/>                                                                                                                                                                                                                 |
| \_\_INTRÍNSECOS DE XM SVML \_\_     | Novedad de DirectXMath 3.16. <br/> Con VS 2019 o versiones posteriores, esto permite a la biblioteca usar la biblioteca Intel &reg; Short Vector Matrix Library para x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
