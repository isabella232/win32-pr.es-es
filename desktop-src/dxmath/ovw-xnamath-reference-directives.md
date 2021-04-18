---
description: Las directivas de compilador ajustan la funcionalidad que utiliza la biblioteca de DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Directivas de compilador de biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f1d67ecd4772116a3bf29f802c39b2e348fd5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705951"
---
# <a name="directxmath-library-compiler-directives"></a>Directivas de compilador de biblioteca DirectXMath

Las directivas de compilador ajustan la funcionalidad que utiliza la biblioteca de DirectXMath.



| Directiva                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_no \_ intrínsecos de XM\_        | Cuando \_ \_ \_ se define XM no intrínsecos \_ , las operaciones de DirectXMath se implementan sin usar intrínsecos específicos de la plataforma. En su lugar, DirectXMath solo usa operaciones de punto flotante estándar.<br/> De forma predeterminada \_ , \_ \_ no se define ningún intrínseco de XM \_ .<br/> Esta directiva invalida todas las demás directivas. Por lo tanto, se recomienda comprobar \_ \_ la ausencia de \_ intrínsecos de XM \_ antes de determinar el estado de los intrínsecos de \_ neón de XM \_ ARM o los \_ \_ \_ \_ \_ intrínsecos de XM SSE \_ \_ .<br/>                                                                              |
| \_\_intrínsecos de XM SSE \_\_       | Cuando \_ \_ se define el intrínseco de XM SSE \_ , el \_ código se compila para usar la compatibilidad con SSE y SSE2 en plataformas que admiten estos conjuntos de instrucciones.<br/> Las versiones de Windows que proporcionan intrínsecos SSE admiten SSE y SSE2.<br/> \_\_ \_ Los intrínsecos de XM SSE no \_ tienen ningún efecto en los sistemas que no admiten SSE y SSE2.<br/> De forma predeterminada \_ , \_ \_ se definen las funciones intrínsecas de XM SSE \_ cuando los usuarios se compilan para una plataforma Windows.<br/> DirectXMath usa el compilador estándar define ( \_ m \_ IX86/ \_ m \_ AMD64) para determinar los destinos de Windows x86 o Windows x64.<br/> |
| \_\_ \_ intrínsecos de neón ARM de XM \_\_ | Esto indica los usos de implementación de DirectXMath de los intrínsecos ARM-neón. De forma predeterminada \_ , \_ \_ \_ se definen las funciones intrínsecas de neón ARM \_ de XM cuando los usuarios se compilan para una plataforma de Windows RT. DirectXMath usa la definición del compilador estándar ( \_ m \_ ARM, \_ m \_ ARM64) para determinar este destino binario.<br/> ARM: la compatibilidad con intrínsecos de neón es nueva en DirectXMath y no es compatible con XNAMath 2. x.<br/>                                                                                                                                                                             |
| \_\_Intrínsecos de XM SSE3 \_\_      | Nuevo para el SDK de Windows 10 Creators Update. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos de SSE3 cuando corresponda. en caso contrario, usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_\_Intrínsecos de XM SSE4 \_\_      | Nuevo para el SDK de aniversario de Windows 10.<br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3 y SSE 4.1, si procede. en caso contrario, usa SSE/SSE2. Cuando se especifica esta directiva de compilador, también se implican los \_ \_ \_ intrínsecos de XM SSE3 \_ y los \_ \_ intrínsecos de XM SSE \_ \_ .<br/>                                                                                                                                                                                                                                |
| \_\_ \_ funciones intrínsecas de XM AVX\_       | Nuevo para el SDK de aniversario de Windows 10.<br/> El uso de/Arch: AVX habilitará esta Directiva. <br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3, SSE 4.1 y AVX 128-bit, si procede. en caso contrario, DirectXMath usa SSE/SSE2. Cuando se especifica esta directiva de compilador, también se implican los \_ \_ \_ intrínsecos de XM SSE3, los \_ intrínsecos de XM \_ SSE4 \_ y los \_ \_ intrínsecos de XM \_ SSE \_ \_ , e incluye un pequeño subconjunto de instrucciones de SSE3. <br/>                                                                    |
| \_Intrínsecos de XM AVX2 \_\_        | Novedades del SDK de Windows 10 Fall Creators Update<br/> El uso de/Arch: AVX2 habilita esta Directiva. Cuando se especifica esta directiva de compilador, las funciones de DirectXMath hacen uso de los intrínsecos AVX2, F16C/CVT16, FMA3, AVX 128-bit, SSE 4.1 y SSE3, si procede. Cuando se usan \_ las \_ \_ funciones intrínsecas \_ de XM AVX2, esto implica \_ \_ \_ funciones intrínsecas de XM F16C \_ , intrínsecos de FMA3 de XM, intrínsecos de XM AVX, intrínsecos de XM SSE, intrínsecos de \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ XM \_ SSE3 \_ \_ y \_ \_ intrínsecos de XM SSE4 \_ \_ .<br/>                                                                                       |
| \_\_Intrínsecos de XM F16C \_\_      | Nuevo para el SDK de aniversario de Windows 10.<br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath se implementan para hacer uso de los intrínsecos SSE3, SSE 4.1, AVX 128-bit y F16C/CVT16, si procede. en caso contrario, DirectXMath usa SSE/SSE2. Cuando se usan \_ las \_ \_ funciones intrínsecas de XM F16C, esto implica que los intrínsecos de XM AVX, los intrínsecos de XM \_ \_ \_ \_ \_ \_ \_ SSE \_ , los \_ \_ intrínsecos de XM \_ SSE3 y los \_ \_ \_ \_ intrínsecos de SSE4 de XM \_ \_ .<br/>                                                                                                                                                 |
| \_\_Intrínsecos de XM FMA3 \_\_      | Novedades del SDK de Windows 10 Fall Creators Update<br/> Cuando se especifica esta directiva de compilador, las funciones de DirectXMath harán uso de los intrínsecos SSE3, SSE 4.1, AVX 128-bit y FMA3, cuando proceda. en caso contrario, DirectXMath usa SSE/SSE2. Cuando se usan \_ las \_ \_ funciones intrínsecas de XM FMA3, esto implica que los intrínsecos de XM AVX, los intrínsecos de XM \_ \_ \_ \_ \_ \_ \_ SSE \_ , los \_ \_ intrínsecos de XM \_ SSE3 y los \_ \_ \_ \_ intrínsecos de SSE4 de XM \_ \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Esto permite el uso de la nueva \_ \_ Convención de llamada vectorcall para destinos Windows x86 o Windows x64. El valor predeterminado es \_ XM \_ VECTORCALL \_ = 1 cuando el compilador admite esta característica. Puede establecerlo manualmente en \_ XM \_ VECTORCALL \_ = 0 para deshabilitarlo siempre. <br/> \_\_vectorcall no se admite para la plataforma Windows RT o C++ administrado. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 




