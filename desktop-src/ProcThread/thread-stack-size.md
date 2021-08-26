---
description: Cada nuevo subproceso o fibra recibe su propio espacio de pila que consta de memoria reservada e inicialmente comprometida.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Tamaño de pila de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031415"
---
# <a name="thread-stack-size"></a>Tamaño de pila de subprocesos

Cada nuevo subproceso o fibra recibe su propio espacio de pila que consta de memoria reservada e inicialmente comprometida. El tamaño de memoria reservada representa la asignación total de la pila en la memoria virtual. Por lo tanto, el tamaño reservado se limita al intervalo de direcciones virtuales. Las páginas que se confirman inicialmente no usan memoria física hasta que se hace referencia a ellas. sin embargo, quitan páginas del límite total de confirmación del sistema, que es el tamaño del archivo de página más el tamaño de la memoria física. El sistema confirma páginas adicionales de la memoria de pila reservada a medida que son necesarias, hasta que la pila alcanza el tamaño reservado menos una página (que se usa como página de protección para evitar el desbordamiento de la pila) o el sistema tiene tan poca memoria que se produce un error en la operación.

Es mejor elegir un tamaño de pila lo más pequeño posible y confirmar la pila necesaria para que el subproceso o la fibra se ejecuten de forma confiable. Todas las páginas reservadas para la pila no se pueden usar para ningún otro propósito.

Una pila se libera cuando se cierra su subproceso. No se libera si otro subproceso finaliza el subproceso.

El tamaño predeterminado de la memoria de pila reservada e inicialmente confirmado se especifica en el encabezado del archivo ejecutable. Se produce un error en la creación de subprocesos o fibras si no hay suficiente memoria para reservar o confirmar el número de bytes solicitados. El tamaño predeterminado de la reserva de pila utilizado por el vinculador es de 1 MB. Para especificar un tamaño de reserva de pila predeterminado diferente para todos los subprocesos y fibras, use la instrucción STACKSIZE en el archivo de definición de módulo (.def). El sistema operativo redondea el tamaño especificado al múltiplo más cercano de la granularidad de asignación del sistema (normalmente 64 KB). Para recuperar la granularidad de asignación del sistema actual, use la [**función GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

Para cambiar el espacio de pila confirmado inicialmente, use el parámetro *dwStackSize* de la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) [**o CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber) Este valor se redondea a la página más cercana. Por lo general, el tamaño de reserva es el tamaño de reserva predeterminado especificado en el encabezado ejecutable. Sin embargo, si el tamaño confirmado inicialmente especificado por *dwStackSize* es mayor o igual que el tamaño de reserva predeterminado, el tamaño de reserva es este nuevo tamaño de confirmación redondeado al múltiplo más cercano de 1 MB.

Para cambiar el tamaño de pila reservado, establezca el parámetro *dwCreationFlags* de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) en STACK SIZE PARAM IS A RESERVATION y use el \_ parámetro \_ \_ \_ \_ *dwStackSize.* En este caso, el tamaño confirmado inicialmente es el tamaño predeterminado especificado en el encabezado ejecutable. Para fibras, use el *parámetro dwStackReserveSize* [**de CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex). El tamaño confirmado se especifica en el *parámetro dwStackCommitSize.*

La [**función SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) establece el tamaño mínimo de la pila asociado al subproceso o fibra que realiza la llamada que estará disponible durante las excepciones de desbordamiento de pila.

 

 
