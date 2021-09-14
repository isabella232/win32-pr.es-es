---
title: Usar matrices, cadenas y punteros
description: El programa Doctor (consulte los ejemplos rpc doctor en el Kit de desarrollo de software de plataforma \\ \\ (SDK)) es un buen ejemplo de una aplicación que muestra los intercambios de diseño implicados con los atributos de matriz y \\ cadena.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071370"
---
# <a name="using-arrays-strings-and-pointers"></a>Usar matrices, cadenas y punteros

El programa Doctor (consulte los ejemplos rpc doctor en el Kit de desarrollo de software de plataforma \\ \\ (SDK)) es un buen ejemplo de una aplicación que muestra los intercambios de diseño implicados con los atributos de matriz y \\ cadena. El programa Doctor es una pequeña versión de ejemplo de un programa más conocido, Eliza, desarrollado por el investigador de inteligencia artificial Dr. Weizenbaum en MIT en la décadas de 1960. El programa imita a un reo al usar la coincidencia de patrones simple para responder a la entrada de lenguaje natural.

El programa Eliza registró la sesión siguiente.



| Usuario                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Todos los hombres son iguales.                                  | ¿De qué manera?                                              |
| Siempre nos están depurando sobre algo u otro. | ¿Puede pensar en un ejemplo específico?                      |
| Bueno, mi padre me hizo llegar aquí.               | Su experiencia le hizo llegar aquí.                        |
| Dice que estoy deprimido gran parte del tiempo.             | Me da pena saber que está deprimido.                |
| Es cierto, no me preocupa.                            | ¿Cree que llegar aquí le ayudará a no ser inconforme? |
| Necesito ayuda; parece seguro.          | ¿Qué significaría para usted si tiene ayuda?           |
| Quizás podría aprender a llevarme bien con mi madre.  | Cuénteme más sobre su familia.                           |
| Mi madre se encarga de mí.                         | Quién cuándolo en su familia se encarga de usted?                |
| Mi padre.                                          | Tu padre.                                              |
| Usted es como mi padre de alguna manera.                | ¿Qué parecido ve?                              |



 

El programa Doctor se puede dividir en aplicaciones del lado cliente y del lado servidor. El lado cliente solicita al paciente la entrada y muestra la respuesta del médico. El lado servidor procesa la entrada del paciente y genera la respuesta del médico. Este es un ejemplo clásico de una aplicación cliente-servidor: el cliente es responsable de la interacción del usuario, mientras que el servidor controla la carga de cálculo extensa. La función no pasa muchos datos y los devuelve, pero, dado que los datos pueden requerir una cantidad significativa de procesamiento, el servidor los procesa.

El programa Doctor usa una matriz de caracteres para la entrada y devuelve otra matriz de caracteres como salida. En la tabla siguiente se enumeran cuatro maneras de pasar matrices de caracteres entre el cliente y el servidor, así como los atributos y funciones necesarios para implementar cada enfoque.



| Enfoque                       | Atributos o funciones                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Matrices de caracteres con recuento       | \[[size \_ es](/windows/desktop/Midl/size-is) \] , length \[ [ \_ es](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Cadenas administradas por código auxiliar           | \[[string](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) on server                  |
| Cadenas administradas por código auxiliar           | \[[string](/windows/desktop/Midl/string) \] , \[ [unique](/windows/desktop/Midl/unique) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) on client and server |
| Función que devuelve una cadena | \[[único](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Dentro de las restricciones asociadas a estas combinaciones de atributos, hay maneras alternativas de enviar una matriz de caracteres del cliente al servidor y de devolver otra matriz de caracteres del servidor al cliente.

En los temas siguientes se muestran los equilibrios de diseño entre las distintas interfaces que pueden administrar estos parámetros.

-   [Matrices de caracteres con recuento](counted-character-arrays.md)
-   [Cadenas](strings.md)
-   [Varios niveles de punteros](multiple-levels-of-pointers.md)

 

 