---
title: Punteros de referencia
description: Los punteros de referencia son los punteros más simples y requieren la menor cantidad de procesamiento que el código auxiliar del cliente.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078252"
---
# <a name="reference-pointers"></a><span data-ttu-id="08ac9-103">Punteros de referencia</span><span class="sxs-lookup"><span data-stu-id="08ac9-103">Reference Pointers</span></span>

<span data-ttu-id="08ac9-104">Los punteros de referencia son los punteros más simples y requieren la menor cantidad de procesamiento que el código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="08ac9-104">Reference pointers are the simplest pointers and require the least amount of processing by the client stub.</span></span> <span data-ttu-id="08ac9-105">Cuando un programa cliente pasa un puntero de referencia a un procedimiento remoto, el puntero de referencia siempre contiene la dirección de un bloque de memoria válido.</span><span class="sxs-lookup"><span data-stu-id="08ac9-105">When a client program passes a reference pointer to a remote procedure, the reference pointer always contains the address of a valid block of memory.</span></span> <span data-ttu-id="08ac9-106">Seguirá señalando al mismo bloque de memoria cuando se complete el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="08ac9-106">It will still be pointing to the same memory block when the remote procedure completes.</span></span> <span data-ttu-id="08ac9-107">Estos punteros se utilizan principalmente para implementar la semántica de referencia y para permitir parámetros \[ [**out**](/windows/desktop/Midl/out-idl) \] en C.</span><span class="sxs-lookup"><span data-stu-id="08ac9-107">These pointers are mainly used to implement reference semantics, and to allow for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters in C.</span></span>

<span data-ttu-id="08ac9-108">En el ejemplo siguiente, el valor del puntero no cambia durante la llamada, aunque el contenido de los datos en la dirección indicada por el puntero puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="08ac9-108">In the following example, the value of the pointer does not change during the call, although the contents of the data at the address indicated by the pointer can change.</span></span>

![cambio de datos en una dirección de puntero de referencia estática](images/prog-a07.png)

<span data-ttu-id="08ac9-110">Un puntero de referencia tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="08ac9-110">A reference pointer has the following characteristics:</span></span>

-   <span data-ttu-id="08ac9-111">Siempre apunta a un almacenamiento válido y nunca tiene el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="08ac9-111">It always points to valid storage and never has the value **NULL**.</span></span>
-   <span data-ttu-id="08ac9-112">Nunca cambia durante una llamada y siempre apunta al mismo almacenamiento antes y después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="08ac9-112">It never changes during a call and always points to the same storage before and after the call.</span></span>
-   <span data-ttu-id="08ac9-113">Los datos devueltos del procedimiento remoto se escriben en el almacenamiento existente.</span><span class="sxs-lookup"><span data-stu-id="08ac9-113">Data returned from the remote procedure is written into the existing storage.</span></span>
-   <span data-ttu-id="08ac9-114">No se puede tener acceso al almacenamiento al que apunta un puntero de referencia a través de otro puntero o cualquier otro nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="08ac9-114">The storage pointed to by a reference pointer cannot be accessed by any other pointer or any other name in the function.</span></span>

<span data-ttu-id="08ac9-115">Utilice el \[ [](/windows/desktop/Midl/ref) \] atributo ref para especificar punteros de referencia en definiciones de interfaz, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="08ac9-115">Use the \[[**ref**](/windows/desktop/Midl/ref)\] attribute to specify reference pointers in interface definitions, as shown in the following example.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

<span data-ttu-id="08ac9-116">En este ejemplo se define el parámetro *pChar* como un puntero a un carácter único, no una matriz de caracteres.</span><span class="sxs-lookup"><span data-stu-id="08ac9-116">This example defines the parameter *pChar* as a pointer to a single character, not an array of characters.</span></span> <span data-ttu-id="08ac9-117">Es un \[  \] parámetro de salida y un puntero de referencia que apunta a la memoria que la rutina de servidor RemoteFn rellenará con los datos.</span><span class="sxs-lookup"><span data-stu-id="08ac9-117">It is an \[**out**\] parameter and a reference pointer that points to memory that the server routine RemoteFn will fill with data.</span></span>

 

 