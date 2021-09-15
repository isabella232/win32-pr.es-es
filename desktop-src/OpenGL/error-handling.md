---
title: Control de errores (OpenGL)
description: Cuando OpenGL detecta un error, registra un código de error actual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Control de errores de OpenGL
- Control de errores de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473684"
---
# <a name="error-handling-opengl"></a>Control de errores (OpenGL)

Cuando OpenGL detecta un error, registra un código de error actual. La función que produjo el error se omite, por lo que no tiene ningún efecto en el estado OpenGL ni en el contenido del búfer de fotogramas. (Si el error registrado era GL \_ SIN \_ \_ MEMORIA, sin embargo, los resultados de la función son indefinidos). Una vez registrado, el código de error actual no se borra hasta que se llama a la función de consulta [**glGetError,**](glgeterror.md) que devuelve el código de error actual.

Las implementaciones de OpenGL pueden devolver varios códigos de error actuales, cada uno de los cuales permanece establecido hasta que se consulta. La **función glGetError** devuelve GL NO ERROR una vez que se han consultado todos los códigos de error actuales o si \_ no hay ningún \_ error. Por lo tanto, si obtiene un código de error, llame **a glGetError** hasta que se devuelva GL NO ERROR para asegurarse de que ha detectado \_ todos los \_ errores. Para obtener la lista de códigos de error, vea [Códigos de error de OpenGL.](opengl-error-codes.md)

Puede usar la función [**GLU gluErrorString**](gluerrorstring.md) para obtener una cadena descriptiva correspondiente al código de error pasado. Para obtener más información sobre **gluErrorString**, vea [Controlar errores.](handling-errors.md)

> [!Note]  
> Las funciones GLU suelen devolver valores de error si se detecta un error. Además, la biblioteca de la utilidad OpenGL define los códigos de error GLU INVALID ENUM, GLU INVALID VALUE y GLU OUT OF MEMORY, que tienen el mismo significado que los códigos de \_ \_ error de \_ \_ \_ \_ \_ OpenGL relacionados.

 

 

 




