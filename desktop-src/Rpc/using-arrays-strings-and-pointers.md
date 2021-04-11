---
title: Usar matrices, cadenas y punteros
description: El programa doctor (consulte \\ ejemplos \\ \\ de RPC doctor en el kit de desarrollo de software (SDK) de la plataforma) es un buen ejemplo de una aplicación que muestra las ventajas e inconvenientes del diseño implicados en los atributos de cadena y matriz.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149335"
---
# <a name="using-arrays-strings-and-pointers"></a>Usar matrices, cadenas y punteros

El programa doctor (consulte \\ ejemplos \\ \\ de RPC doctor en el kit de desarrollo de software (SDK) de la plataforma) es un buen ejemplo de una aplicación que muestra las ventajas e inconvenientes del diseño implicados en los atributos de cadena y matriz. El programa doctor es una pequeña versión de ejemplo de un programa más conocido, Eliza, desarrollado por el investigador de inteligencia artificial Joseph Weizenbaum en MIT en los años 60. El programa imita un therapist mediante el uso de la coincidencia de patrones simple para responder a la entrada de lenguaje natural.

El programa Eliza registró la sesión siguiente.



| User (Usuario)                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Los hombres son todo por igual.                                  | ¿De qué manera?                                              |
| Siempre nos molesta sobre algo u otros. | ¿Puede pensar en un ejemplo específico?                      |
| Bueno, mi Boyfriend me apareció aquí.               | Su Boyfriend ha llegado a su disposición.                        |
| Indica que me he despresionado mucho tiempo.             | Me encanta oír que está presionado.                |
| Es cierto que estoy insatisfecho.                            | ¿Cree que en este caso le ayudará a no estar insatisfecho? |
| Necesito ayuda; eso parece cierto.          | ¿Qué quiere decir si tiene alguna ayuda?           |
| Quizás aprenda a trabajar con mi madre.  | Más información acerca de la familia.                           |
| Mi madre se encarga de mí.                         | ¿Quién más se encarga de su familia?                |
| Mi padre.                                          | Su padre.                                              |
| Es como mi padre de algunas maneras.                | ¿Qué similitud se ve?                              |



 

El programa doctor puede dividirse en aplicaciones cliente y en el lado servidor. El lado cliente solicita la entrada al paciente y muestra la respuesta del médico. El lado servidor procesa la entrada del paciente y genera la respuesta del médico. Este es un ejemplo clásico de una aplicación cliente-servidor: el cliente es responsable de la interacción con el usuario mientras el servidor controla la carga de cálculo exhaustiva. No se pasan muchos datos a la función y los devuelven, pero, dado que los datos pueden requerir una cantidad significativa de procesamiento, el servidor los procesa.

El programa doctor usa una matriz de caracteres para la entrada y devuelve otra matriz de caracteres como salida. En la tabla siguiente se enumeran cuatro maneras de pasar matrices de caracteres entre el cliente y el servidor, así como los atributos y las funciones necesarias para implementar cada enfoque.



| Enfoque                       | Atributos o funciones                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Matrices de caracteres contables       | \[[el tamaño \_ es](/windows/desktop/Midl/size-is) \] , la \[ [longitud \_ es](/windows/desktop/Midl/length-is) \] , la \[ [referencia](/windows/desktop/Midl/ref)\]                                         |
| Cadenas administradas por código auxiliar           | \[[cadena](/windows/desktop/Midl/string) \] , \[ [referencia](/windows/desktop/Midl/ref) \] , [ \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1) en el servidor                  |
| Cadenas administradas por código auxiliar           | \[[String](/windows/desktop/Midl/string) \] , \[ [Unique](/windows/desktop/Midl/unique) \] , el [usuario de MIDL se \_ \_ asigna](/windows/desktop/Midl/midl-user-allocate-1) en el cliente y el servidor |
| Función que devuelve una cadena | \[[único](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Dentro de las restricciones asociadas a estas combinaciones de atributos, existen formas alternativas de enviar una matriz de caracteres del cliente al servidor y devolver otra matriz de caracteres del servidor al cliente.

En los temas siguientes se muestran las ventajas e inconvenientes del diseño entre las distintas interfaces que pueden administrar estos parámetros.

-   [Matrices de caracteres contables](counted-character-arrays.md)
-   [Cadenas](strings.md)
-   [Varios niveles de punteros](multiple-levels-of-pointers.md)

 

 