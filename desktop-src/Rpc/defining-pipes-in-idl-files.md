---
title: Definir canalizaciones en archivos IDL
description: Cuando se define una canalización en un archivo IDL, el compilador MIDL genera una estructura de control de canalización cuyos miembros son punteros a procedimientos de inserción, extracción y asignación, así como a una variable de estado que coordina estos procedimientos.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421083"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="cb955-103">Definir canalizaciones en archivos IDL</span><span class="sxs-lookup"><span data-stu-id="cb955-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="cb955-104">Cuando se define una canalización en un archivo IDL, el compilador MIDL genera una estructura de control de canalización cuyos miembros son punteros a procedimientos de inserción, extracción y asignación, así como a una variable de estado que coordina estos procedimientos.</span><span class="sxs-lookup"><span data-stu-id="cb955-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="cb955-105">La aplicación cliente inicializa los campos en la estructura de control de canalización, mantiene su variable de estado y administra la transferencia de datos con sus propias funciones de inserción, extracción y asignación.</span><span class="sxs-lookup"><span data-stu-id="cb955-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="cb955-106">El código auxiliar de cliente llama a estas funciones de aplicación en bucles durante la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="cb955-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="cb955-107">En el caso de una canalización de entrada, el código auxiliar del cliente calcula las referencias de los datos de transferencia y los transmite al código auxiliar del servidor.</span><span class="sxs-lookup"><span data-stu-id="cb955-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="cb955-108">En el caso de una canalización de salida, el código auxiliar de cliente no calcula las referencias de los datos en un búfer y pasa un puntero a ese búfer de vuelta a la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cb955-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="cb955-109">El código de código auxiliar del servidor inicializa los campos de la estructura del control de canalización en una variable de estado, así como punteros a rutinas de inserción y extracción.</span><span class="sxs-lookup"><span data-stu-id="cb955-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="cb955-110">El código auxiliar del servidor mantiene el estado y administra su almacenamiento privado para los datos de transferencia.</span><span class="sxs-lookup"><span data-stu-id="cb955-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="cb955-111">La aplicación de servidor llama a las rutinas de extracción e inserción en bucles durante la llamada a procedimiento remoto, ya que recibe y anula las referencias a los datos del código auxiliar del cliente, o calcula las referencias y transmite los datos al código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="cb955-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="cb955-112">En el siguiente archivo IDL de ejemplo se define una canalización de tipo de canalización larga \_ , cuyo tamaño de elemento se define como **Long**.</span><span class="sxs-lookup"><span data-stu-id="cb955-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="cb955-113">También declara prototipos de función para el procedimiento remoto llama a la incanalización y la sobrecanalización, para enviar y recibir datos, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cb955-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="cb955-114">Cuando el compilador MIDL procesa el archivo IDL, genera el archivo de encabezado que se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cb955-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="cb955-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb955-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="cb955-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb955-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb955-117">codo</span><span class="sxs-lookup"><span data-stu-id="cb955-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="cb955-118">**/OI**</span><span class="sxs-lookup"><span data-stu-id="cb955-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 