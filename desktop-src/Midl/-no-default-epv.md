---
title: modificador/no_default_epv
description: El \_ modificador de EPV predeterminado de/no \_ indica al compilador de MIDL que no genere un vector de punto de entrada predeterminado (EPV). No se recomienda el uso de este atributo.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv modificador MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995143"
---
# <a name="no_default_epv-switch"></a><span data-ttu-id="b4ae5-105">/no \_ \_ modificador EPV predeterminado</span><span class="sxs-lookup"><span data-stu-id="b4ae5-105">/no\_default\_epv switch</span></span>

<span data-ttu-id="b4ae5-106">El modificador de **\_ \_ EPV predeterminado de/no** indica al compilador de MIDL que no genere un vector de punto de entrada predeterminado (EPV).</span><span class="sxs-lookup"><span data-stu-id="b4ae5-106">The **/no\_default\_epv** switch directs the MIDL compiler not to generate a default entry-point vector (epv).</span></span> <span data-ttu-id="b4ae5-107">No se recomienda el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="b4ae5-107">The use of this attribute is not recommended.</span></span>

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a><span data-ttu-id="b4ae5-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="b4ae5-108">Switch Options</span></span>

<span data-ttu-id="b4ae5-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b4ae5-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ae5-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b4ae5-110">Remarks</span></span>

<span data-ttu-id="b4ae5-111">En este caso, la aplicación debe registrar un EPV con la llamada a [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .</span><span class="sxs-lookup"><span data-stu-id="b4ae5-111">In this case, the application must register an epv with the [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) call.</span></span> <span data-ttu-id="b4ae5-112">Compare este modificador con el modificador [**\_ EPV de/use**](-use-epv.md) .</span><span class="sxs-lookup"><span data-stu-id="b4ae5-112">Compare this switch with the [**/use\_epv**](-use-epv.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="b4ae5-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4ae5-113">Examples</span></span>

<span data-ttu-id="b4ae5-114">**MIDL/no \_ default \_ EPV nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="b4ae5-114">**midl /no\_default\_epv filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b4ae5-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4ae5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4ae5-116">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="b4ae5-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b4ae5-117">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="b4ae5-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b4ae5-118">**/Use \_ EPV**</span><span class="sxs-lookup"><span data-stu-id="b4ae5-118">**/use\_epv**</span></span>](-use-epv.md)
</dt> <dt>

[<span data-ttu-id="b4ae5-119">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="b4ae5-119">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 