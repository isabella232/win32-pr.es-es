---
description: Solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como namespacepath. Si se usan el modificador del espacio de nombres MOF-n del compilador y el \# espacio de nombres pragma&\# 32; el comando namespacepath, el comando tiene prioridad sobre el modificador.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma (espacio de nombres)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811414"
---
# <a name="pragma-namespace"></a><span data-ttu-id="81e4b-104">pragma (espacio de nombres)</span><span class="sxs-lookup"><span data-stu-id="81e4b-104">pragma namespace</span></span>

<span data-ttu-id="81e4b-105">El comando **pragma namespace** Preprocessing solicita que el compilador cargue el archivo MOF en el espacio de nombres especificado como *namespacepath*.</span><span class="sxs-lookup"><span data-stu-id="81e4b-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="81e4b-106">Si se usan el modificador del espacio de nombres MOF **-n** del compilador y el comando **\# pragma namespace** *namespacepath* , el comando tiene prioridad sobre el modificador.</span><span class="sxs-lookup"><span data-stu-id="81e4b-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="81e4b-107">A continuación se describe la sintaxis:</span><span class="sxs-lookup"><span data-stu-id="81e4b-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="81e4b-108">El *\[ espacio de nombres \]* es el espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="81e4b-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="81e4b-109">Si no especifica este comando ni el modificador de línea de comandos equivalente, el compilador MOF usará el \\ espacio de nombres predeterminado raíz de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="81e4b-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e4b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81e4b-110">Remarks</span></span>

<span data-ttu-id="81e4b-111">Puede requerir que las aplicaciones y los scripts de cliente usen una conexión cifrada para la autenticación agregando el calificador **RequiresEncryption** al archivo. mof que crea el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="81e4b-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="81e4b-112">También puede modificar un espacio de nombres existente agregando este atributo y compilar de nuevo el archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="81e4b-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="81e4b-113">Para obtener más información sobre cómo usar **RequiresEncryption**, vea [requerir una conexión cifrada a un espacio de nombres](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="81e4b-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="81e4b-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="81e4b-114">Examples</span></span>

<span data-ttu-id="81e4b-115">En el ejemplo siguiente se muestra cómo colocar clases o instancias en el espacio de nombres "raíz de \\ prueba".</span><span class="sxs-lookup"><span data-stu-id="81e4b-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="81e4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81e4b-116">Requirements</span></span>



| <span data-ttu-id="81e4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81e4b-117">Requirement</span></span> | <span data-ttu-id="81e4b-118">Value</span><span class="sxs-lookup"><span data-stu-id="81e4b-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="81e4b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81e4b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81e4b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81e4b-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="81e4b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81e4b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81e4b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81e4b-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81e4b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="81e4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e4b-124">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="81e4b-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="81e4b-125">**Calificadores WMI estándar**</span><span class="sxs-lookup"><span data-stu-id="81e4b-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="81e4b-126">Comandos de preprocesador</span><span class="sxs-lookup"><span data-stu-id="81e4b-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




