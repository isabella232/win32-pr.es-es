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
# <a name="using-serialization-services"></a><span data-ttu-id="c138b-104">Usar servicios de serialización</span><span class="sxs-lookup"><span data-stu-id="c138b-104">Using Serialization Services</span></span>

<span data-ttu-id="c138b-105">MIDL genera un código auxiliar de serialización para el procedimiento con los atributos \[ [**codificar**](/windows/desktop/Midl/encode) \] y \[ [**descodificar**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="c138b-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="c138b-106">Cuando se llama a esta rutina, se ejecuta una llamada de serialización en lugar de una llamada remota.</span><span class="sxs-lookup"><span data-stu-id="c138b-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="c138b-107">Se calculan las referencias de los argumentos del procedimiento o se anula su serialización desde un búfer de la manera habitual.</span><span class="sxs-lookup"><span data-stu-id="c138b-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="c138b-108">A continuación, tendrá el control completo de los búferes.</span><span class="sxs-lookup"><span data-stu-id="c138b-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="c138b-109">Por el contrario, cuando el programa realiza la serialización de tipos (un tipo se etiqueta con atributos de serialización), MIDL genera rutinas para ajustar el tamaño, codificar y descodificar objetos de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="c138b-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="c138b-110">Para serializar los datos, debe llamar a estas rutinas de la manera adecuada.</span><span class="sxs-lookup"><span data-stu-id="c138b-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="c138b-111">La serialización de tipo es una extensión de Microsoft y, como tal, no está disponible al compilar en modo de compatibilidad de DCE ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="c138b-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="c138b-112">Mediante el uso de los \[ atributos [**codificar**](/windows/desktop/Midl/encode) \] y \[ [**descodificar**](/windows/desktop/Midl/decode) \] como atributos de interfaz, RPC aplica la codificación a todos los tipos y rutinas definidos en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c138b-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="c138b-113">Debe proporcionar los búferes alineados correctamente al usar los servicios de serialización.</span><span class="sxs-lookup"><span data-stu-id="c138b-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="c138b-114">El principio del búfer debe estar alineado en una dirección que sea un múltiplo de 8 o 8 bytes alineados.</span><span class="sxs-lookup"><span data-stu-id="c138b-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="c138b-115">Para la serialización de procedimientos, cada llamada de procedimiento debe calcular las referencias de una posición de búfer o una vez que no las calcule.</span><span class="sxs-lookup"><span data-stu-id="c138b-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="c138b-116">Para la serialización de tipo, el ajuste de tamaño, la codificación y la descodificación deben comenzar en una posición alineada de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="c138b-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="c138b-117">Una manera de que la aplicación garantice que sus búferes están alineados es escribir la función de [**\_ \_ asignación de usuarios de MIDL**](/windows/desktop/Midl/midl-user-allocate-1) para que cree búferes alineados.</span><span class="sxs-lookup"><span data-stu-id="c138b-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="c138b-118">En el ejemplo de código siguiente se muestra cómo se puede hacer esto.</span><span class="sxs-lookup"><span data-stu-id="c138b-118">The following code sample demonstrates how this can be done.</span></span>


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



<span data-ttu-id="c138b-119">En el ejemplo siguiente se muestra la función [**\_ \_ libre de usuario de MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c138b-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


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



 

 