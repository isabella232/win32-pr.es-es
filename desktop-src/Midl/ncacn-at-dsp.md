---
title: ncacn_at_dsp atributo)
description: La \_ \_ palabra clave ncacn at DSP identifica AppleTalk DSP como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995217"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="08767-105">ncacn \_ en el \_ atributo DSP</span><span class="sxs-lookup"><span data-stu-id="08767-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="08767-106">La palabra clave **ncacn \_ at \_ DSP** identifica AppleTalk DSP como la familia de protocolos para el extremo.</span><span class="sxs-lookup"><span data-stu-id="08767-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="08767-107">Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.</span><span class="sxs-lookup"><span data-stu-id="08767-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="08767-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08767-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08767-109">*nombre del puerto*</span><span class="sxs-lookup"><span data-stu-id="08767-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08767-110">Especifica una cadena de caracteres de hasta 22 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="08767-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08767-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08767-111">Remarks</span></span>

<span data-ttu-id="08767-112">La sintaxis de la cadena de puerto de DSP de AppleTalk, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL.</span><span class="sxs-lookup"><span data-stu-id="08767-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="08767-113">El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta.</span><span class="sxs-lookup"><span data-stu-id="08767-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="08767-114">Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="08767-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="08767-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08767-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="08767-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="08767-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08767-117">**finales**</span><span class="sxs-lookup"><span data-stu-id="08767-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="08767-118">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="08767-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="08767-119">**enlace de cadenas**</span><span class="sxs-lookup"><span data-stu-id="08767-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 