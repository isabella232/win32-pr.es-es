---
title: ncacn_dnet_nsp atributo)
description: La \_ \_ palabra clave ncacn dnet NSP identifica DECnet como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149255"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="8f631-105">\_ \_ atributo NSP de ncacn dnet</span><span class="sxs-lookup"><span data-stu-id="8f631-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="8f631-106">La palabra clave **ncacn \_ dnet \_ NSP** identifica DECnet como la familia de protocolos para el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="8f631-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="8f631-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="8f631-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="8f631-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f631-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f631-109">*nombre del servidor*</span><span class="sxs-lookup"><span data-stu-id="8f631-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8f631-110">Especifica el nombre o la dirección de Internet del servidor, o host, del equipo.</span><span class="sxs-lookup"><span data-stu-id="8f631-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="8f631-111">El nombre es una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8f631-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="8f631-112">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="8f631-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8f631-113">Especifica un nombre de objeto de DECnet o un número de objeto.</span><span class="sxs-lookup"><span data-stu-id="8f631-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="8f631-114">El nombre del objeto puede constar de hasta 16 caracteres.</span><span class="sxs-lookup"><span data-stu-id="8f631-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="8f631-115">Los números de objeto pueden ir precedidos del signo de almohadilla ( \# ).</span><span class="sxs-lookup"><span data-stu-id="8f631-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f631-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f631-116">Remarks</span></span>

<span data-ttu-id="8f631-117">La sintaxis de la cadena de puerto de transporte DECnet, como todas las cadenas de puerto, se define independientemente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="8f631-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="8f631-118">El compilador realiza algunas comprobaciones de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="8f631-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="8f631-119">Es posible que se notifiquen algunos errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="8f631-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="8f631-120">Esta familia de protocolos no se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8f631-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8f631-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f631-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="8f631-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f631-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f631-123">**finales**</span><span class="sxs-lookup"><span data-stu-id="8f631-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="8f631-124">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="8f631-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 