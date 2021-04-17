---
description: En esta sección se proporciona una lista de los códigos de retorno, las constantes simbólicas, los valores literales y las descripciones de WMI. Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o comandos de WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696779"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="f6fbf-104">Códigos de retorno de WMI</span><span class="sxs-lookup"><span data-stu-id="f6fbf-104">WMI Return Codes</span></span>

<span data-ttu-id="f6fbf-105">En esta sección se proporciona una lista de los códigos de retorno, las constantes simbólicas, los valores literales y las descripciones de WMI.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="f6fbf-106">Estos códigos pueden ser devueltos por scripts, aplicaciones de C++ o comandos de [**WMIC**](wmic.md) .</span><span class="sxs-lookup"><span data-stu-id="f6fbf-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="f6fbf-107">Si se produce un error, WMI devuelve uno de los siguientes códigos de error como un valor de 32 bits en el que los dos bits de orden superior indican el código de gravedad del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="f6fbf-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="f6fbf-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="f6fbf-109">Correcto</span><span class="sxs-lookup"><span data-stu-id="f6fbf-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="f6fbf-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="f6fbf-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="f6fbf-111">Informativo</span><span class="sxs-lookup"><span data-stu-id="f6fbf-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="f6fbf-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="f6fbf-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="f6fbf-113">Advertencia</span><span class="sxs-lookup"><span data-stu-id="f6fbf-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="f6fbf-114"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="f6fbf-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="f6fbf-115">Error</span><span class="sxs-lookup"><span data-stu-id="f6fbf-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="f6fbf-116">Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="f6fbf-117">Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="f6fbf-118">En cualquier circunstancia, no elimine el repositorio WMI como primera acción, ya que la eliminación del repositorio puede provocar daños en el sistema o en las aplicaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="f6fbf-119">Para obtener más información sobre el origen del problema, puede descargar y ejecutar la herramienta de línea de comandos de diagnóstico de [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="f6fbf-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="f6fbf-120">Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="f6fbf-121">El informe también ayuda a los servicios de soporte técnico de Microsoft para ayudarle.</span><span class="sxs-lookup"><span data-stu-id="f6fbf-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="f6fbf-122">Puede descargar el Utilidad de diagnóstico de WMI [aquí](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="f6fbf-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="f6fbf-123">**Constantes de error de WMI**</span><span class="sxs-lookup"><span data-stu-id="f6fbf-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="f6fbf-124">**Constantes que no son de error de WMI**</span><span class="sxs-lookup"><span data-stu-id="f6fbf-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



