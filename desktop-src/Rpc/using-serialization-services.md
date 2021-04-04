---
title: Usar servicios de serialización
description: MIDL genera un código auxiliar de serialización para el procedimiento con los atributos \ encode \ y \ decode \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC llamada a procedimiento remoto, tareas, uso de servicios de serialización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078324"
---
# <a name="using-serialization-services"></a>Usar servicios de serialización

MIDL genera un código auxiliar de serialización para el procedimiento con los atributos \[ [**codificar**](/windows/desktop/Midl/encode) \] y \[ [**descodificar**](/windows/desktop/Midl/decode) \] . Cuando se llama a esta rutina, se ejecuta una llamada de serialización en lugar de una llamada remota. Se calculan las referencias de los argumentos del procedimiento o se anula su serialización desde un búfer de la manera habitual. A continuación, tendrá el control completo de los búferes.

Por el contrario, cuando el programa realiza la serialización de tipos (un tipo se etiqueta con atributos de serialización), MIDL genera rutinas para ajustar el tamaño, codificar y descodificar objetos de ese tipo. Para serializar los datos, debe llamar a estas rutinas de la manera adecuada. La serialización de tipo es una extensión de Microsoft y, como tal, no está disponible al compilar en modo de compatibilidad de DCE ([**/OSF**](/windows/desktop/Midl/-osf)). Mediante el uso de los \[ atributos [**codificar**](/windows/desktop/Midl/encode) \] y \[ [**descodificar**](/windows/desktop/Midl/decode) \] como atributos de interfaz, RPC aplica la codificación a todos los tipos y rutinas definidos en el archivo IDL.

Debe proporcionar los búferes alineados correctamente al usar los servicios de serialización. El principio del búfer debe estar alineado en una dirección que sea un múltiplo de 8 o 8 bytes alineados. Para la serialización de procedimientos, cada llamada de procedimiento debe calcular las referencias de una posición de búfer o una vez que no las calcule. Para la serialización de tipo, el ajuste de tamaño, la codificación y la descodificación deben comenzar en una posición alineada de 8 bytes.

Una manera de que la aplicación garantice que sus búferes están alineados es escribir la función de [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) para que cree búferes alineados. En el ejemplo de código siguiente se muestra cómo se puede hacer esto.


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



En el ejemplo siguiente se muestra la función [**\_ \_ libre de usuario de MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondiente.


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



 

 