---
title: Identificadores de enlace automáticos
description: Los identificadores de enlace automáticos son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener ninguna información de estado entre el cliente y el servidor.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359300"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="414c3-103">Identificadores de enlace automáticos</span><span class="sxs-lookup"><span data-stu-id="414c3-103">Automatic Binding Handles</span></span>

<span data-ttu-id="414c3-104">Los identificadores de enlace automáticos son útiles cuando la aplicación no requiere un servidor específico y cuando no necesita mantener ninguna información de estado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="414c3-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="414c3-105">Cuando se usa un controlador de enlace automático, no es necesario escribir ningún código de aplicación cliente para tratar con enlaces y identificadores; basta con especificar el uso del identificador de enlace automático en el archivo de configuración de la aplicación (ACF).</span><span class="sxs-lookup"><span data-stu-id="414c3-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="414c3-106">A continuación, el código auxiliar define el identificador y administra el enlace.</span><span class="sxs-lookup"><span data-stu-id="414c3-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="414c3-107">Por ejemplo, una operación de marca de tiempo se puede implementar mediante un identificador automático.</span><span class="sxs-lookup"><span data-stu-id="414c3-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="414c3-108">No hace ninguna diferencia con la aplicación cliente qué servidor la proporciona con la marca de tiempo, ya que puede aceptar el tiempo de cualquier servidor disponible.</span><span class="sxs-lookup"><span data-stu-id="414c3-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="414c3-109">Los identificadores automáticos no se admiten para la plataforma Macintosh.</span><span class="sxs-lookup"><span data-stu-id="414c3-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="414c3-110">Para especificar el uso de identificadores automáticos, incluya el \[ atributo de [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) \] en el ACF.</span><span class="sxs-lookup"><span data-stu-id="414c3-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="414c3-111">En el ejemplo de marca de tiempo se usa el ACF siguiente:</span><span class="sxs-lookup"><span data-stu-id="414c3-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="414c3-112">Cuando el ACF no incluye ningún otro atributo de identificador y cuando los procedimientos remotos no utilizan identificadores explícitos, el compilador de MIDL usa identificadores automáticos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="414c3-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="414c3-113">También utiliza identificadores automáticos como valor predeterminado cuando el ACF no está presente.</span><span class="sxs-lookup"><span data-stu-id="414c3-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="414c3-114">Los procedimientos remotos se especifican en el archivo IDL.</span><span class="sxs-lookup"><span data-stu-id="414c3-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="414c3-115">El identificador automático no debe aparecer como argumento para el procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="414c3-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="414c3-116">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="414c3-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="414c3-117">La ventaja del identificador automático es que el desarrollador no tiene que escribir código para administrar el identificador; el código auxiliar administra el enlace automáticamente.</span><span class="sxs-lookup"><span data-stu-id="414c3-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="414c3-118">Esto es significativamente diferente del [ejemplo Hello, World](tutorial.md), donde el cliente administra el identificador primitivo implícito definido en ACF y debe llamar a varias funciones en tiempo de ejecución para establecer el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="414c3-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 