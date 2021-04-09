---
title: enable_allocate atributo)
description: El atributo \ enable \_ allocate especifica que el código auxiliar del servidor debe habilitar el entorno de administración de memoria de código auxiliar.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate el atributo MIDL
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149206"
---
# <a name="enable_allocate-attribute"></a><span data-ttu-id="b76c4-104">habilitar \_ asignar atributo</span><span class="sxs-lookup"><span data-stu-id="b76c4-104">enable\_allocate attribute</span></span>

<span data-ttu-id="b76c4-105">El atributo **\[ habilitar \_ asignar \]** ACF especifica que el código auxiliar de servidor debe habilitar el entorno de administración de memoria de código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="b76c4-105">The **\[enable\_allocate\]** ACF attribute specifies that the server stub code should enable the stub memory management environment.</span></span>

> [!Note]  
> <span data-ttu-id="b76c4-106">El atributo **\[ enable \_ allocate \]** está obsoleto y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="b76c4-106">The **\[enable\_allocate\]** attribute is obsolete and is no longer supported.</span></span>

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a><span data-ttu-id="b76c4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b76c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b76c4-108">*opcional-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b76c4-108">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b76c4-109">Especifica una lista de cero o más atributos MIDL adicionales.</span><span class="sxs-lookup"><span data-stu-id="b76c4-109">Specifies a list of zero or more additional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="b76c4-110">*nombre de interfaz*</span><span class="sxs-lookup"><span data-stu-id="b76c4-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b76c4-111">El nombre de la interfaz a la que se aplicará el atributo **\[ enable \_ allcoate \]** .</span><span class="sxs-lookup"><span data-stu-id="b76c4-111">The name of the interface to which the **\[enable\_allcoate\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b76c4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b76c4-112">Remarks</span></span>

<span data-ttu-id="b76c4-113">En el modo predeterminado, el código auxiliar de servidor habilita el entorno de memoria solo cuando se usa el atributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="b76c4-113">In default mode, the server stub enables the memory environment only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="b76c4-114">El entorno de administración de memoria debe estar habilitado para poder asignar memoria mediante [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span><span class="sxs-lookup"><span data-stu-id="b76c4-114">The memory management environment must be enabled before memory can be allocated using [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate).</span></span> <span data-ttu-id="b76c4-115">En el modo de **OSF** (al compilar mediante el modificador [**/OSF**](-osf.md) ), el código auxiliar habilita este entorno automáticamente, o bien, si se solicita, se usa el atributo **\[ habilitar \_ asignación \]** .</span><span class="sxs-lookup"><span data-stu-id="b76c4-115">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the stub enables this environment automatically, or on request when the **\[enable\_allocate\]** attribute is used.</span></span>

<span data-ttu-id="b76c4-116">El código auxiliar del lado cliente puede ser sensible al entorno de administración de memoria **RPCSS** .</span><span class="sxs-lookup"><span data-stu-id="b76c4-116">The client side stub may be sensitive to the **Rpcss** memory management environment.</span></span> <span data-ttu-id="b76c4-117">Si se ejecuta un código auxiliar de cliente confidencial cuando se deshabilita el paquete **RPCSS** , se llama al asignador o desasignadores de usuario predeterminado (por ejemplo, el [usuario de MIDL \_ \_ asigna](/windows/desktop/Rpc/the-midl-user-allocate-function)el /  [usuario de MIDL \_ \_ gratis](/windows/desktop/Rpc/the-midl-user-free-function)).</span><span class="sxs-lookup"><span data-stu-id="b76c4-117">If a sensitive client stub is executed when the **Rpcss** package is disabled, the default user allocator/deallocators are called (for example, [midl\_user\_allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)/ [midl\_user\_free](/windows/desktop/Rpc/the-midl-user-free-function)).</span></span> <span data-ttu-id="b76c4-118">Cuando está habilitado, el paquete **RPCSS** usa el par allocator/desasignador del paquete.</span><span class="sxs-lookup"><span data-stu-id="b76c4-118">When enabled, the **Rpcss** package uses the allocator/deallocator pair from the package.</span></span> <span data-ttu-id="b76c4-119">En el modo predeterminado, el cliente es sensible solo cuando se usa el atributo **\[ enable \_ allocate \]** .</span><span class="sxs-lookup"><span data-stu-id="b76c4-119">In the default mode, the client is sensitive only when the **\[enable\_allocate\]** attribute is used.</span></span> <span data-ttu-id="b76c4-120">Normalmente, el código auxiliar del lado cliente funciona en el entorno deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b76c4-120">Typically, the client side stub operates in the disabled environment.</span></span> <span data-ttu-id="b76c4-121">En el modo de **OSF** (al compilar mediante el modificador [**/OSF**](-osf.md) ), el cliente siempre es sensible al entorno de administración de memoria **RPCSS** y, por lo tanto, el atributo **\[ enable \_ allocate \]** no afectará al código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="b76c4-121">In **osf** mode (when you compile using the [**/osf**](-osf.md) switch), the client is always sensitive to the **Rpcss** memory management environment and, therefore, the **\[enable\_allocate\]** attribute will not affect the client stubs.</span></span>

## <a name="see-also"></a><span data-ttu-id="b76c4-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b76c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b76c4-123">Archivo de configuración de la aplicación (ACF)</span><span class="sxs-lookup"><span data-stu-id="b76c4-123">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b76c4-124">\_asignación de usuarios de MIDL \_</span><span class="sxs-lookup"><span data-stu-id="b76c4-124">midl\_user\_allocate</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="b76c4-125">usuario de MIDL \_ \_ gratis</span><span class="sxs-lookup"><span data-stu-id="b76c4-125">midl\_user\_free</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="b76c4-126">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b76c4-126">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="b76c4-127">RpcSmDisableAllocate</span><span class="sxs-lookup"><span data-stu-id="b76c4-127">RpcSmDisableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[<span data-ttu-id="b76c4-128">RpcSmEnableAllocate</span><span class="sxs-lookup"><span data-stu-id="b76c4-128">RpcSmEnableAllocate</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[<span data-ttu-id="b76c4-129">RpcSmFree</span><span class="sxs-lookup"><span data-stu-id="b76c4-129">RpcSmFree</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 