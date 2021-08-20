---
description: La memoria que pertenece a un proceso está protegida implícitamente por su espacio de direcciones virtuales privadas.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Protección de la memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4421b07ee4ed88dffe0e46d1121d5d4117b471a84ffcf4f85738bd8be912f09c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809079"
---
# <a name="memory-protection"></a>Protección de la memoria

La memoria que pertenece a un proceso está protegida implícitamente por su espacio de direcciones virtuales privadas. Además, Windows protección de memoria mediante el hardware de memoria virtual. La implementación de esta protección varía con el procesador, por ejemplo, las páginas de códigos del espacio de direcciones de un proceso se pueden marcar como de solo lectura y protegerse frente a modificaciones por subprocesos en modo de usuario.

Para obtener la lista completa de atributos, vea [Constantes de protección de memoria.](memory-protection-constants.md)

## <a name="copy-on-write-protection"></a>Protección de copia en escritura

La protección de copia en escritura es una optimización que permite que varios procesos asignen sus espacios de direcciones virtuales de modo que compartan una página física hasta que uno de los procesos modifique la página. Esto forma parte de una técnica denominada *evaluación* diferida , que permite al sistema conservar la memoria física y el tiempo al no realizar una operación hasta que sea absolutamente necesario.

Por ejemplo, suponga que dos procesos cargan páginas del mismo archivo DLL en sus espacios de memoria virtual. Estas páginas de memoria virtual se asignan a las mismas páginas de memoria física para ambos procesos. Siempre que ninguno de los procesos escriba en estas páginas, puede asignarlas y compartirlas, las mismas páginas físicas, como se muestra en el diagrama siguiente.

![cuadros y flechas del proceso 1 y 2 páginas asignadas a la misma memoria física](images/mem1.png)

Si el proceso 1 escribe en una de estas páginas, el contenido de la página física se copia en otra página física y la asignación de memoria virtual se actualiza para el proceso 1. Ambos procesos ahora tienen su propia instancia de la página en memoria física. Por lo tanto, no es posible que un proceso escriba en una página física compartida y que el otro proceso vea los cambios.

![cuadros y flechas de procesos y remapping de memoria física](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Carga de aplicaciones y archivos DLL

Cuando se cargan varias instancias de la misma aplicación basada en Windows, cada instancia se ejecuta en su propio espacio de direcciones virtuales protegidas. Sin embargo, sus identificadores de instancia (*hInstance*) normalmente tienen el mismo valor. Este valor representa la dirección base de la aplicación en su espacio de direcciones virtuales. Si cada instancia se puede cargar en su dirección base predeterminada, puede asignar y compartir las mismas páginas físicas con las otras instancias mediante la protección de copia en escritura. El sistema permite que estas instancias compartan las mismas páginas físicas hasta que una de ellas modifique una página. Si, por algún motivo, una de estas instancias no se puede cargar en la dirección base deseada, recibe sus propias páginas físicas.

Los archivos DLL se crean con una dirección base predeterminada. Cada proceso que usa un archivo DLL intentará cargar el archivo DLL dentro de su propio espacio de direcciones en la dirección virtual predeterminada del archivo DLL. Si varias aplicaciones pueden cargar un archivo DLL en su dirección virtual predeterminada, pueden compartir las mismas páginas físicas para el archivo DLL. Si por algún motivo un proceso no puede cargar el archivo DLL en la dirección predeterminada, carga el archivo DLL en otro lugar. La protección de copia en escritura obliga a que algunas de las páginas del archivo DLL se copien en páginas físicas diferentes para este proceso, ya que las correcciones de las instrucciones de salto se escriben dentro de las páginas del archivo DLL y serán diferentes para este proceso. Si la sección de código contiene muchas referencias a la sección de datos, esto puede hacer que toda la sección de código se copie en nuevas páginas físicas.

 

 



