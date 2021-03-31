---
title: Serialización de búfer fijo
description: Serialización de búfer fija.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418780"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="aed25-103">Serialización de búfer fijo</span><span class="sxs-lookup"><span data-stu-id="aed25-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="aed25-104">Cuando use el estilo de búfer fijo, especifique un búfer lo suficientemente grande como para alojar las operaciones de codificación (serialización) realizadas con el identificador.</span><span class="sxs-lookup"><span data-stu-id="aed25-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="aed25-105">Al anular la serialización, se proporciona el búfer que contiene todos los datos que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="aed25-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="aed25-106">El estilo de búfer fijo de serialización utiliza las siguientes rutinas:</span><span class="sxs-lookup"><span data-stu-id="aed25-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="aed25-107">**MesEncodeFixedBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="aed25-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="aed25-108">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="aed25-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="aed25-109">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="aed25-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="aed25-110">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="aed25-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="aed25-111">La función **MesEncodeFixedBufferHandleCreate** asigna la memoria necesaria para el controlador de codificación y, a continuación, la inicializa.</span><span class="sxs-lookup"><span data-stu-id="aed25-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="aed25-112">La aplicación puede llamar a [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar el identificador, o puede llamar a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar la memoria del controlador.</span><span class="sxs-lookup"><span data-stu-id="aed25-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="aed25-113">Para crear un identificador de descodificación que se corresponda con el identificador de codificación de estilo fijo, debe utilizar [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="aed25-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="aed25-114">La aplicación llama a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar el identificador de búfer de codificación o descodificación.</span><span class="sxs-lookup"><span data-stu-id="aed25-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="aed25-115">Ejemplos de codificación de búfer fija</span><span class="sxs-lookup"><span data-stu-id="aed25-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="aed25-116">En la sección siguiente se proporciona un ejemplo de cómo usar un estilo de búfer fijo: serialización de un identificador para la codificación de procedimientos.</span><span class="sxs-lookup"><span data-stu-id="aed25-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="aed25-117">El siguiente fragmento representa una parte de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="aed25-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="aed25-118">En la sección siguiente se proporciona un ejemplo de cómo usar un estilo de búfer fijo: serialización de un controlador para la codificación de tipos.</span><span class="sxs-lookup"><span data-stu-id="aed25-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="aed25-119">El siguiente fragmento representa los fragmentos de aplicación pertinentes.</span><span class="sxs-lookup"><span data-stu-id="aed25-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




