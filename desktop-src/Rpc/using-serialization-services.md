---
title: Uso de servicios de serialización
description: MIDL genera un código auxiliar de serialización para el procedimiento con los atributos \ encode\ y \ decode\ .
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- Procedimiento remoto Llame a RPC , tareas, mediante servicios de serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be20d513bdb74eca316b022dd8536e8988e32e93099981cc77830035048e55e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010642"
---
# <a name="using-serialization-services"></a>Uso de servicios de serialización

MIDL genera un código auxiliar de serialización para el procedimiento con los atributos \[ [**codificar**](/windows/desktop/Midl/encode) \] y \[ [**descodificar**](/windows/desktop/Midl/decode) \] . Cuando se llama a esta rutina, se ejecuta una llamada de serialización en lugar de una llamada remota. Los argumentos de procedimiento se serializan a o se desmarshalen desde un búfer de la manera habitual. A continuación, tendrá el control completo de los búferes.

Por el contrario, cuando el programa realiza la serialización de tipos (un tipo se etiqueta con atributos de serialización), MIDL genera rutinas para cambiar el tamaño, codificar y descodificar objetos de ese tipo. Para serializar los datos, debe llamar a estas rutinas de la manera adecuada. La serialización de tipos es una extensión de Microsoft y, como tal, no está disponible cuando se compila en modo de compatibilidad con DCE ([**/osf).**](/windows/desktop/Midl/-osf) Mediante el uso de los atributos de codificación y descodificación como atributos de interfaz, RPC aplica la codificación a todos los tipos y \[ [](/windows/desktop/Midl/encode) \] \[ [](/windows/desktop/Midl/decode) \] rutinas definidos en el archivo IDL.

Debe proporcionar búferes alineados adecuadamente al usar servicios de serialización. El principio del búfer debe alinearse en una dirección que sea un múltiplo de 8 u 8 bytes alineado. Para la serialización de procedimientos, cada llamada a procedimiento debe serializar en o desmarshal desde una posición de búfer alineada de 8 bytes. Para la serialización de tipos, el tamaño, la codificación y la codificación deben comenzar en una posición alineada de 8 bytes.

Una manera de que la aplicación se asegure de que sus búferes están alineados es escribir la función de asignación de usuario intermedio para que cree búferes alineados. [**\_ \_**](/windows/desktop/Midl/midl-user-allocate-1) En el ejemplo de código siguiente se muestra cómo se puede hacer esto.


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



En el ejemplo siguiente se muestra la [**función gratuita de usuario midl \_ \_**](/windows/desktop/Midl/midl-user-free-1) correspondiente.


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 