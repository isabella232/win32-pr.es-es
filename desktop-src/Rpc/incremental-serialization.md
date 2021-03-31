---
title: Serialización incremental
description: Cuando se usa la serialización de estilo incremental, se proporcionan tres rutinas para manipular el búfer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532403"
---
# <a name="incremental-serialization"></a><span data-ttu-id="10e7f-103">Serialización incremental</span><span class="sxs-lookup"><span data-stu-id="10e7f-103">Incremental Serialization</span></span>

<span data-ttu-id="10e7f-104">Cuando se usa la serialización de estilo incremental, se proporcionan tres rutinas para manipular el búfer.</span><span class="sxs-lookup"><span data-stu-id="10e7f-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="10e7f-105">Estas rutinas son: Alloc, Read y Write.</span><span class="sxs-lookup"><span data-stu-id="10e7f-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="10e7f-106">La rutina de asignación asigna un búfer del tamaño requerido.</span><span class="sxs-lookup"><span data-stu-id="10e7f-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="10e7f-107">La rutina Write escribe los datos en el búfer y la rutina Read recupera un búfer que contiene los datos de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="10e7f-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="10e7f-108">Una única llamada de serialización puede realizar varias llamadas a estas rutinas.</span><span class="sxs-lookup"><span data-stu-id="10e7f-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="10e7f-109">El estilo incremental de serialización utiliza las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="10e7f-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="10e7f-110">**MesEncodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="10e7f-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="10e7f-111">**MesDecodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="10e7f-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="10e7f-112">**MesIncrementalHandleReset**</span><span class="sxs-lookup"><span data-stu-id="10e7f-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="10e7f-113">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="10e7f-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="10e7f-114">A continuación se muestran los prototipos de las funciones de asignación, lectura y escritura que debe proporcionar:</span><span class="sxs-lookup"><span data-stu-id="10e7f-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

<span data-ttu-id="10e7f-115">La entrada de estado un parámetro para las tres funciones es el puntero definido por la aplicación que estaba asociado al identificador de servicios de codificación.</span><span class="sxs-lookup"><span data-stu-id="10e7f-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="10e7f-116">La aplicación puede utilizar este puntero para obtener acceso a la estructura que contiene información específica de la aplicación, como un identificador de archivo o un puntero de secuencia.</span><span class="sxs-lookup"><span data-stu-id="10e7f-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="10e7f-117">Tenga en cuenta que el código auxiliar no modifica el puntero de estado que no sea para pasarlo a las funciones de asignación, lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="10e7f-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="10e7f-118">Durante la codificación, se llama a Alloc para obtener un búfer en el que se serializan los datos.</span><span class="sxs-lookup"><span data-stu-id="10e7f-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="10e7f-119">A continuación, se llama a write para permitir que la aplicación controle cuándo y dónde se almacenan los datos serializados.</span><span class="sxs-lookup"><span data-stu-id="10e7f-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="10e7f-120">Durante la descodificación, se llama a Read para devolver el número solicitado de bytes de datos serializados desde donde la aplicación la almacenó.</span><span class="sxs-lookup"><span data-stu-id="10e7f-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="10e7f-121">Una característica importante del estilo incremental es que el identificador mantiene el puntero de estado automáticamente.</span><span class="sxs-lookup"><span data-stu-id="10e7f-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="10e7f-122">Este puntero mantiene el estado y nunca lo tocan las funciones RPC, excepto cuando se pasa el puntero a la función de asignación, escritura o lectura.</span><span class="sxs-lookup"><span data-stu-id="10e7f-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="10e7f-123">El identificador también mantiene un estado interno que permite codificar y descodificar varias instancias de tipo en el mismo búfer agregando el relleno según sea necesario para la alineación.</span><span class="sxs-lookup"><span data-stu-id="10e7f-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="10e7f-124">La función [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) restablece un identificador a su estado inicial para habilitar la lectura o escritura desde el principio del búfer.</span><span class="sxs-lookup"><span data-stu-id="10e7f-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="10e7f-125">Las funciones de asignación y escritura, junto con un puntero definido por la aplicación, están asociadas a un identificador de servicios de codificación mediante una llamada a la función [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) .</span><span class="sxs-lookup"><span data-stu-id="10e7f-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="10e7f-126">**MesEncodeIncrementalHandleCreate** asigna la memoria necesaria para el identificador y, a continuación, la inicializa.</span><span class="sxs-lookup"><span data-stu-id="10e7f-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="10e7f-127">La aplicación puede llamar a [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) para crear un identificador de descodificación, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) para reinicializar el identificador o [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del controlador.</span><span class="sxs-lookup"><span data-stu-id="10e7f-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="10e7f-128">La función Read, junto con un parámetro definido por la aplicación, está asociada a un identificador de descodificación mediante una llamada a la rutina **MesDecodeIncrementalHandleCreate** .</span><span class="sxs-lookup"><span data-stu-id="10e7f-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="10e7f-129">La función crea el identificador y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="10e7f-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="10e7f-130">Los parámetros UserState, Alloc, Write y Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) pueden ser **null** para indicar que no hay cambios.</span><span class="sxs-lookup"><span data-stu-id="10e7f-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




