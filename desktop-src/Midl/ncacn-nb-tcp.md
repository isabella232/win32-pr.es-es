---
title: ncacn_nb_tcp atributo)
description: La \_ \_ palabra clave TCP de ncacn NB se usa para identificar TCP sobre NetBIOS como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358928"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="bc073-105">\_ \_ atributo TCP de ncacn NB</span><span class="sxs-lookup"><span data-stu-id="bc073-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="bc073-106">La palabra clave **\_ \_ TCP de ncacn NB** se usa para identificar TCP sobre NetBIOS como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="bc073-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="bc073-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="bc073-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="bc073-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc073-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc073-109">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="bc073-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bc073-110">Especifica un valor de 8 bits opcional comprendido entre 1 y 254.</span><span class="sxs-lookup"><span data-stu-id="bc073-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="bc073-111">Los valores de menor que 0x20 están reservados.</span><span class="sxs-lookup"><span data-stu-id="bc073-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="bc073-112">Si no se especifica el valor de *nombre de Puerto* , el servicio de asignación de puntos de conexión selecciona el valor de puerto.</span><span class="sxs-lookup"><span data-stu-id="bc073-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc073-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc073-113">Remarks</span></span>

<span data-ttu-id="bc073-114">La sintaxis de la cadena de puerto NetBIOS, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación IDL.</span><span class="sxs-lookup"><span data-stu-id="bc073-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="bc073-115">El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="bc073-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="bc073-116">Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="bc073-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="bc073-117">Esta familia de protocolos no se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc073-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bc073-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bc073-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="bc073-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc073-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc073-120">**finales**</span><span class="sxs-lookup"><span data-stu-id="bc073-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="bc073-121">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="bc073-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bc073-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="bc073-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="bc073-123">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="bc073-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="bc073-124">**NP de ncacn \_**</span><span class="sxs-lookup"><span data-stu-id="bc073-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="bc073-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="bc073-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="bc073-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="bc073-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="bc073-127">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="bc073-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 