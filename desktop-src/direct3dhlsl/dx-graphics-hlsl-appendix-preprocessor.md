---
title: Directivas de preprocesador (HLSL)
description: Las directivas de preprocesador, como \ define y \ ifdef, se utilizan normalmente para que los programas de origen sean fáciles de cambiar y compilar en diferentes entornos de ejecución.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800572"
---
# <a name="preprocessor-directives-hlsl"></a>Directivas de preprocesador (HLSL)

Las directivas de preprocesador, como [ \# define](dx-graphics-hlsl-appendix-pre-define.md) y [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), se utilizan normalmente para que los programas de origen sean fáciles de cambiar y compilar en diferentes entornos de ejecución. Las directivas del archivo de código fuente indican al preprocesador que realice acciones específicas. Por ejemplo, el preprocesador puede reemplazar tokens en el texto, insertar el contenido de otros archivos en el archivo de código fuente o suprimir la compilación de parte del archivo quitando secciones de texto. Las líneas de preprocesador se reconocen y se ejecutan antes de la expansión de macro. Por consiguiente, si una macro se expande en algo que se parezca a un comando de preprocesador, el preprocesador no reconocerá ese comando.

Las instrucciones de preprocesador utilizan el mismo juego de caracteres que las instrucciones del archivo de código fuente, con la excepción de que no se admiten secuencias de escape. El juego de caracteres utilizado en las instrucciones de preprocesador es el mismo que el juego de caracteres de la ejecución. El preprocesador también reconoce valores de caracteres negativos.

El preprocesador HLSL reconoce las siguientes directivas:

-   [\#define](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#error](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#Cuando](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#inclui](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#Ondula](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#UNDEF](dx-graphics-hlsl-appendix-pre-undef.md)

El signo de número ( \# ) debe ser el primer carácter que no sea un espacio en blanco en la línea que contiene la Directiva; los caracteres de espacio en blanco pueden aparecer entre el signo de número y la primera letra de la Directiva. Algunas directivas incluyen argumentos o valores. Cualquier texto que siga a una directiva (excepto un argumento o un valor que forme parte de la Directiva) debe ir precedido por el delimitador de comentario de una sola línea (//) o incluido entre delimitadores de comentario (/ \* \* /). Las líneas que contienen directivas de preprocesador pueden continuar inmediatamente antes del marcador de fin de línea con una barra diagonal inversa ( \) .

Las directivas de preprocesador pueden aparecer en cualquier lugar de un archivo de código fuente, pero solo se aplican al resto del archivo de código fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




