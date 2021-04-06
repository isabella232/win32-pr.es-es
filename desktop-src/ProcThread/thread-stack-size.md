---
description: Cada nuevo subproceso o fibra recibe su propio espacio de pila compuesto por la memoria reservada y inicialmente asignada.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Tamaño de pila de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4204e0bffa13fb43b6ea9520b60c0505372bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002137"
---
# <a name="thread-stack-size"></a>Tamaño de pila de subprocesos

Cada nuevo subproceso o fibra recibe su propio espacio de pila compuesto por la memoria reservada y inicialmente asignada. El tamaño de memoria reservada representa la asignación total de la pila en la memoria virtual. Como tal, el tamaño reservado se limita al intervalo de direcciones virtuales. Las páginas confirmadas inicialmente no usan la memoria física hasta que se hace referencia a ellas. sin embargo, quitan páginas del límite total de confirmaciones del sistema, que es el tamaño del archivo de paginación más el tamaño de la memoria física. El sistema confirma páginas adicionales de la memoria reservada de la pila a medida que se necesitan, hasta que la pila alcanza el tamaño reservado menos una página (que se usa como una página de protección para evitar el desbordamiento de la pila) o el sistema es tan bajo en la memoria que la operación no se realiza correctamente.

Es mejor elegir el tamaño de la pila como sea posible y confirmar la pila necesaria para que el subproceso o la fibra se ejecuten de forma confiable. Todas las páginas reservadas para la pila no se pueden usar para ningún otro propósito.

Una pila se libera cuando se cierra su subproceso. No se libera si otro subproceso finaliza el subproceso.

El tamaño predeterminado de la memoria de pila reservada y inicialmente confirmada se especifica en el encabezado del archivo ejecutable. Se produce un error en la creación de subprocesos o fibras si no hay suficiente memoria para reservar o confirmar el número de bytes solicitados. El tamaño de reserva de pila predeterminado utilizado por el enlazador es 1 MB. Para especificar un tamaño de reserva de pila predeterminado diferente para todos los subprocesos y fibras, use la instrucción STACKSIZE en el archivo de definición de módulo (. def). El sistema operativo redondea el tamaño especificado al múltiplo más cercano de la granularidad de asignación del sistema (normalmente 64 KB). Para recuperar la granularidad de asignación del sistema actual, utilice la función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Para cambiar el espacio de pila inicialmente confirmado, use el parámetro *dwStackSize* de la función [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)o [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) . Este valor se redondea hacia arriba a la página más cercana. Por lo general, el tamaño de reserva es el tamaño de reserva predeterminado especificado en el encabezado ejecutable. Sin embargo, si el tamaño inicialmente confirmado especificado por *dwStackSize* es mayor o igual que el tamaño de reserva predeterminado, el tamaño de reserva es este nuevo tamaño de confirmación redondeado al múltiplo más cercano de 1 MB.

Para cambiar el tamaño de la pila reservada, establezca el parámetro *dwCreationFlags* de [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) en el parámetro de tamaño de pila \_ \_ \_ es \_ una \_ reserva y use el parámetro *dwStackSize* . En este caso, el tamaño asignado inicialmente es el tamaño predeterminado especificado en el encabezado ejecutable. Para fibras, use el parámetro *dwStackReserveSize* de [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex). El tamaño confirmado se especifica en el parámetro *dwStackCommitSize* .

La función [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) establece el tamaño mínimo de la pila asociada al subproceso o fibra que realiza la llamada que estará disponible durante cualquier excepción de desbordamiento de pila.

 

 
