---
description: Monitor de red usa la función de exportación de DllMain para identificar la existencia del analizador y liberar recursos que Monitor de red utiliza para almacenar información sobre el analizador.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementar el analizador de DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808689"
---
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="bb843-103">Implementar el analizador de DllMain</span><span class="sxs-lookup"><span data-stu-id="bb843-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="bb843-104">Monitor de red usa la función de exportación de **DllMain** para identificar la existencia del analizador y liberar recursos que monitor de red utiliza para almacenar información sobre el analizador.</span><span class="sxs-lookup"><span data-stu-id="bb843-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="bb843-105">Cuando Monitor de red llama a **DllMain** por primera vez, el archivo DLL del analizador llama a [**CreateProtocol**](createprotocol.md) para hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb843-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="bb843-106">Especifique el protocolo que detecta el analizador.</span><span class="sxs-lookup"><span data-stu-id="bb843-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="bb843-107">Proporcione puntos de entrada para las funciones de exportación de analizador restantes que Monitor de red llamadas.</span><span class="sxs-lookup"><span data-stu-id="bb843-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="bb843-108">Cuando Monitor de red llama a **DllMain** por última vez, **DllMain** llama a [**DestroyProtocol**](destroyprotocol.md) para liberar todos los recursos que monitor de red utiliza para almacenar información sobre el analizador.</span><span class="sxs-lookup"><span data-stu-id="bb843-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="bb843-109">En el procedimiento siguiente se identifican los pasos necesarios para implementar **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="bb843-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="bb843-110">**Para implementar DllMain**</span><span class="sxs-lookup"><span data-stu-id="bb843-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="bb843-111">Especifique la estructura [**ENTRYPOINTS**](entrypoints.md) para la función [**CreateProtocol**](createprotocol.md) y la variable de conexión global.</span><span class="sxs-lookup"><span data-stu-id="bb843-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="bb843-112">La variable Attach se usa para realizar el seguimiento del número de instancias de protocolo que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="bb843-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="bb843-113">Observe el valor del parámetro de *comando* que establece el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bb843-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="bb843-114">Si el parámetro de *comando* se establece en la Asociación de proceso de dll \_ y Attach \_ es 0, llame a [**CreateProtocol**](createprotocol.md) para proporcionar el nombre del protocolo y los puntos de entrada para las siguientes funciones de exportación.</span><span class="sxs-lookup"><span data-stu-id="bb843-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="bb843-115">**Registro**</span><span class="sxs-lookup"><span data-stu-id="bb843-115">**Register**</span></span>
    -   <span data-ttu-id="bb843-116">**Eliminar registro**</span><span class="sxs-lookup"><span data-stu-id="bb843-116">**Deregister**</span></span>
    -   <span data-ttu-id="bb843-117">**RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="bb843-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="bb843-118">**AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="bb843-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="bb843-119">**FormatProperties** (solo es necesario si monitor de red mostrarán las propiedades del Protocolo).</span><span class="sxs-lookup"><span data-stu-id="bb843-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="bb843-120">Si el parámetro de *comando* se establece en \_ la \_ desasociación de proceso de dll y Attach es 0, llame a [**DestroyProtocol**](destroyprotocol.md) con el identificador de instancia que devuelve [**CreateProtocol**](createprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="bb843-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="bb843-121">Devuelve **true** porque la función del analizador **DllMain** siempre debe devolver **true**.</span><span class="sxs-lookup"><span data-stu-id="bb843-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="bb843-122">La siguiente es una implementación básica de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="bb843-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="bb843-123">En el ejemplo de código se usa una instrucción Case para capturar valores del parámetro de *comando* con el fin de determinar si se debe llamar a [**CreateProtocol**](createprotocol.md) o [**DestroyProtocol**](destroyprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="bb843-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



