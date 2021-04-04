---
title: modificador/RPCSS
description: El modificador/RPCSS, cuando se especifica, actúa como si \_ se hubiera especificado el atributo enable Allocate en todas las operaciones de la interfaz. No se recomienda el uso de este atributo.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- /RPCSS modificador MIDL
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076598"
---
# <a name="rpcss-switch"></a><span data-ttu-id="33330-105">modificador/RPCSS</span><span class="sxs-lookup"><span data-stu-id="33330-105">/rpcss switch</span></span>

<span data-ttu-id="33330-106">El modificador **/RPCSS** , cuando se especifica, actúa como si se hubiera especificado el atributo [**enable \_ allocate**](enable-allocate.md) en todas las operaciones de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="33330-106">The **/rpcss** switch, when specified, acts as though the [**enable\_allocate**](enable-allocate.md) attribute was specified on all operations of the interface.</span></span> <span data-ttu-id="33330-107">No se recomienda el uso de este atributo.</span><span class="sxs-lookup"><span data-stu-id="33330-107">The usage of this attribute is not recommended.</span></span>

``` syntax
midl /rpcss
```

## <a name="switch-options"></a><span data-ttu-id="33330-108">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="33330-108">Switch Options</span></span>

<span data-ttu-id="33330-109">Este modificador no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="33330-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="33330-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33330-110">Remarks</span></span>

<span data-ttu-id="33330-111">En el modo predeterminado, el paquete RpcSs solo está habilitado si el procedimiento o la interfaz tiene el atributo [**habilitar \_ asignación**](enable-allocate.md) o el modificador **/RPCSS** se ha especificado en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="33330-111">In default mode, the RpcSs package is enabled only if either the procedure or interface has the [**enable\_allocate**](enable-allocate.md) attribute or the **/rpcss** switch is specified on the command line.</span></span> <span data-ttu-id="33330-112">En el modo **/OSF** , el código auxiliar del lado servidor habilita el paquete de asignación RPCSS.</span><span class="sxs-lookup"><span data-stu-id="33330-112">In **/osf** mode, the server-side stub enables the RpcSs allocation package.</span></span>

## <a name="examples"></a><span data-ttu-id="33330-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="33330-113">Examples</span></span>

<span data-ttu-id="33330-114">**MIDL/RPCSS nombrearchivo. idl**</span><span class="sxs-lookup"><span data-stu-id="33330-114">**midl /rpcss filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="33330-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="33330-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33330-116">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="33330-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="33330-117">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="33330-117">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="33330-118">**habilitar \_ asignación**</span><span class="sxs-lookup"><span data-stu-id="33330-118">**enable\_allocate**</span></span>](enable-allocate.md)
</dt> <dt>

[<span data-ttu-id="33330-119">**/osf**</span><span class="sxs-lookup"><span data-stu-id="33330-119">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 




