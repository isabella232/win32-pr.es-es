---
description: La memoria que pertenece a un proceso está protegida implícitamente por su espacio de direcciones virtuales privado.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Protección de la memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156881"
---
# <a name="memory-protection"></a>Protección de la memoria

La memoria que pertenece a un proceso está protegida implícitamente por su espacio de direcciones virtuales privado. Además, Windows proporciona protección de memoria mediante el uso del hardware de memoria virtual. La implementación de esta protección varía en función del procesador; por ejemplo, las páginas de códigos del espacio de direcciones de un proceso pueden marcarse como de solo lectura y protegerse contra modificaciones realizadas por subprocesos en modo usuario.

Para obtener una lista completa de los atributos, vea [constantes de protección de memoria](memory-protection-constants.md).

## <a name="copy-on-write-protection"></a>Protección de copia en escritura

La protección de copia en escritura es una optimización que permite que varios procesos asignen sus espacios de direcciones virtuales para que compartan una página física hasta que uno de los procesos modifique la página. Esto forma parte de una técnica denominada *evaluación diferida*, que permite que el sistema Ahorre memoria física y tiempo al no realizar una operación hasta que sea absolutamente necesario.

Por ejemplo, suponga que dos procesos cargan páginas del mismo archivo DLL en sus espacios de memoria virtual. Estas páginas de memoria virtual se asignan a las mismas páginas de memoria física para ambos procesos. Siempre y cuando ninguno de los procesos escriba en estas páginas, se pueden asignar y compartir, las mismas páginas físicas, como se muestra en el diagrama siguiente.

![cuadros y flechas del proceso 1 y 2 páginas asignadas a la misma memoria física](images/mem1.png)

Si el proceso 1 escribe en una de estas páginas, el contenido de la página física se copia en otra página física y el mapa de memoria virtual se actualiza para el proceso 1. Ambos procesos tienen ahora su propia instancia de la página en la memoria física. Por lo tanto, no es posible que un proceso escriba en una página física compartida y que el otro proceso vea los cambios.

![cuadros y flechas de procesos y reasignación de memoria física](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Cargar aplicaciones y archivos dll

Cuando se cargan varias instancias de la misma aplicación basada en Windows, cada instancia se ejecuta en su propio espacio de direcciones virtuales protegido. Sin embargo, sus identificadores de instancia (*hInstance*) suelen tener el mismo valor. Este valor representa la dirección base de la aplicación en su espacio de direcciones virtuales. Si cada instancia se puede cargar en su dirección base predeterminada, puede asignar y compartir las mismas páginas físicas con las demás instancias, mediante la protección de copia en escritura. El sistema permite que estas instancias compartan las mismas páginas físicas hasta que una de ellas modifica una página. Si por alguna razón no se puede cargar una de estas instancias en la dirección base deseada, recibirá sus propias páginas físicas.

Los archivos DLL se crean con una dirección base predeterminada. Cada proceso que usa un archivo DLL intentará cargar el archivo DLL en su propio espacio de direcciones en la dirección virtual predeterminada del archivo DLL. Si varias aplicaciones pueden cargar un archivo DLL en su dirección virtual predeterminada, pueden compartir las mismas páginas físicas para el archivo DLL. Si por algún motivo un proceso no puede cargar el archivo DLL en la dirección predeterminada, carga el archivo DLL en otro lugar. La protección de copia en escritura obliga a que algunas de las páginas del archivo DLL se copien en páginas físicas diferentes para este proceso, ya que las correcciones para instrucciones de salto se escriben en las páginas del archivo DLL y serán diferentes para este proceso. Si la sección de código contiene muchas referencias a la sección de datos, esto puede hacer que se copie toda la sección de código en nuevas páginas físicas.

 

 



