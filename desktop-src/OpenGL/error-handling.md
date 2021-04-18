---
title: Control de errores (OpenGL)
description: Cuando OpenGL detecta un error, registra un código de error actual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- control de errores OpenGL
- Control de errores de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105676542"
---
# <a name="error-handling-opengl"></a>Control de errores (OpenGL)

Cuando OpenGL detecta un error, registra un código de error actual. La función que causó el error se omite, por lo que no tiene ningún efecto en el estado de OpenGL o en el contenido de fotogramas. (Si el error registrado es GL \_ \_ \_ Sin embargo, los resultados de la función no están definidos. Una vez registrado, el código de error actual no se borra hasta que se llama a la función de consulta [**glGetError**](glgeterror.md) , que devuelve el código de error actual.

Las implementaciones de OpenGL pueden devolver varios códigos de error actuales, cada uno de los cuales permanece establecido hasta que se consultan. La función **glGetError** devuelve GL \_ no \_ error una vez que ha consultado todos los códigos de error actuales o si no hay ningún error. Por lo tanto, si obtiene un código de error, llame a **glGetError** hasta que \_ no \_ se devuelva ningún error para asegurarse de que ha detectado todos los errores. Para obtener la lista de códigos de error, consulte [códigos de error de OpenGL](opengl-error-codes.md).

Puede usar la función [**gluErrorString**](gluerrorstring.md) Glu para obtener una cadena descriptiva correspondiente al código de error que se pasa. Para obtener más información sobre **gluErrorString**, consulte [control de errores](handling-errors.md).

> [!Note]  
> Las funciones GLU a menudo devuelven valores de error si se detecta un error. Además, la biblioteca de la utilidad OpenGL define los códigos de error GLU \_ \_ enumeración no válida, Glu \_ valor no válido \_ y Glu \_ memoria insuficiente \_ \_ , que tienen el mismo significado que los códigos de error de OpenGL relacionados.

 

 

 




