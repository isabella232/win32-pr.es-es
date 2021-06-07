---
title: Directivas de preprocesador (HLSL)
description: Las directivas de preprocesador, como \ define y \ ifdef, se usan normalmente para que los programas de origen sean fáciles de cambiar y fáciles de compilar en diferentes entornos de ejecución.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386834"
---
# <a name="preprocessor-directives-hlsl"></a>Directivas de preprocesador (HLSL)

Las directivas de preprocesador, como [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef,](dx-graphics-hlsl-appendix-pre-ifdef.md)se usan normalmente para que los programas de origen sean fáciles de cambiar y fáciles de compilar en diferentes entornos de ejecución. Las directivas del archivo de código fuente indican al preprocesador que realice acciones específicas. Por ejemplo, el preprocesador puede reemplazar tokens en el texto, insertar el contenido de otros archivos en el archivo de código fuente o suprimir la compilación de parte del archivo quitando secciones de texto. Las líneas de preprocesador se reconocen y se ejecutan antes de la expansión de macro. Por consiguiente, si una macro se expande en algo que se parezca a un comando de preprocesador, el preprocesador no reconocerá ese comando.

Las instrucciones de preprocesador utilizan el mismo juego de caracteres que las instrucciones del archivo de código fuente, con la excepción de que no se admiten secuencias de escape. El juego de caracteres utilizado en las instrucciones de preprocesador es el mismo que el juego de caracteres de la ejecución. El preprocesador también reconoce valores de caracteres negativos.

El preprocesador HLSL reconoce las siguientes directivas:

-   [\#Definir](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Error](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#Si](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#incluír](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#line](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#Pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

El signo de número ( ) debe ser el primer carácter de espacio no blanco en la línea que contiene la directiva; los caracteres de espacio en blanco pueden aparecer entre el signo de número y la primera letra de \# la directiva. Algunas directivas incluyen argumentos o valores. Cualquier texto que sigue a una directiva (excepto un argumento o valor que forma parte de la directiva) debe ir precedido del delimitador de comentario de una sola línea (//) o incluirse entre delimitadores de comentario (/ \* \* /). Las líneas que contienen directivas de preprocesador se pueden continuar inmediatamente antes del marcador de fin de línea con una barra diagonal inversa ( \\ ).

Las directivas de preprocesador pueden aparecer en cualquier lugar de un archivo de código fuente, pero solo se aplican al resto del archivo de código fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Apéndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




