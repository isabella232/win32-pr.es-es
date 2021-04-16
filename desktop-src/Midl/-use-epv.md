---
title: modificador/use_epv
description: El \_ modificador/use EPV indica al compilador de MIDL que genere código de código auxiliar de servidor que llame a la rutina de aplicación de servidor a través de un vector de punto de entrada (EPV), en lugar de una llamada estática. No se recomienda el uso de este atributo.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv modificador MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105685699"
---
# <a name="use_epv-switch"></a><span data-ttu-id="f9240-105">/Use \_ modificador EPV</span><span class="sxs-lookup"><span data-stu-id="f9240-105">/use\_epv switch</span></span>

<span data-ttu-id="f9240-106">El modificador **/use \_ EPV** indica al compilador de MIDL que genere código de código auxiliar de servidor que llame a la rutina de aplicación de servidor a través de un vector de punto de entrada (EPV), en lugar de una llamada estática.</span><span class="sxs-lookup"><span data-stu-id="f9240-106">The **/use\_epv** switch directs the MIDL compiler to generate server stub code that calls the server application routine through an entry-point vector (epv), rather than by a static call.</span></span> <span data-ttu-id="f9240-107">No se recomienda el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="f9240-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /use_epv
```

## <a name="switch-options"></a><span data-ttu-id="f9240-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="f9240-108">Switch Options</span></span>

<span data-ttu-id="f9240-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f9240-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9240-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9240-110">Remarks</span></span>

<span data-ttu-id="f9240-111">Normalmente, las aplicaciones requieren vinculación estática a la rutina de aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="f9240-111">Typically, applications require static linkage to the server application routine.</span></span> <span data-ttu-id="f9240-112">El compilador MIDL genera este tipo de llamada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f9240-112">The MIDL compiler generates such a call by default.</span></span> <span data-ttu-id="f9240-113">Sin embargo, si una aplicación requiere que el código auxiliar del servidor llame a la rutina de aplicación de servidor mediante EPV, se debe especificar el modificador **\_ EPV de/use** .</span><span class="sxs-lookup"><span data-stu-id="f9240-113">However, if an application requires the server stub to call the server application routine by using the epv, the **/use\_epv** switch must be specified.</span></span> <span data-ttu-id="f9240-114">Cuando se especifica el modificador **/use \_ EPV** , el compilador MIDL genera una EPV predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f9240-114">When the **/use\_epv** switch is specified, the MIDL compiler generates a default epv.</span></span> <span data-ttu-id="f9240-115">Este valor predeterminado de EPV se usa después si la aplicación no registra otro EPV a través de la llamada a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="f9240-115">This default epv is then used if the application does not register another epv through the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span>

## <a name="examples"></a><span data-ttu-id="f9240-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f9240-116">Examples</span></span>

<span data-ttu-id="f9240-117">**MIDL/use \_ EPV** *filename \* \* *. idl**</span><span class="sxs-lookup"><span data-stu-id="f9240-117">**midl /use\_epv** *filename\*\*\*.idl*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="f9240-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9240-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9240-119">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="f9240-119">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="f9240-120">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="f9240-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="f9240-121">**/no \_ default \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="f9240-121">**/no\_default\_epv**</span></span>](-no-default-epv.md)
</dt> <dt>

[<span data-ttu-id="f9240-122">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="f9240-122">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 