---
description: El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de Instrumental de administración de Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI y SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279295"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="e2d11-103">WMI y SNMP</span><span class="sxs-lookup"><span data-stu-id="e2d11-103">WMI and SNMP</span></span>

<span data-ttu-id="e2d11-104">El proveedor del Protocolo simple de administración de redes (SNMP) permite a las aplicaciones cliente obtener acceso a información de SNMP a través de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e2d11-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="e2d11-105">El proveedor SNMP no se instala de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e2d11-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="e2d11-106">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e2d11-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="e2d11-107">El Protocolo simple de administración de redes (SNMP) utiliza un esquema para definir objetos.</span><span class="sxs-lookup"><span data-stu-id="e2d11-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="e2d11-108">El esquema es diferente del esquema utilizado en WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="e2d11-109">El esquema SNMPv1 y SNMPv2C se denomina estructura de la información de administración (SMI) y se empaqueta como archivos de base de información de administración (MIB).</span><span class="sxs-lookup"><span data-stu-id="e2d11-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="e2d11-110">Los archivos MIB definen objetos mediante un lenguaje estándar: notación de sintaxis abstracta 1 (ASN. 1) y varias definiciones de macro que sirven como plantillas para describir los objetos.</span><span class="sxs-lookup"><span data-stu-id="e2d11-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="e2d11-111">Las macros proporcionan información como el nombre del objeto, el identificador, la sintaxis, la descripción, los derechos de acceso, las operaciones del protocolo y la codificación del protocolo.</span><span class="sxs-lookup"><span data-stu-id="e2d11-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="e2d11-112">En la tabla siguiente se muestra cómo el proveedor SNMP controla distintos aspectos de un objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="e2d11-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="e2d11-113">Tema</span><span class="sxs-lookup"><span data-stu-id="e2d11-113">Topic</span></span>                                                    | <span data-ttu-id="e2d11-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2d11-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="e2d11-115">NOTIFICATION-TYPE (macro)</span><span class="sxs-lookup"><span data-stu-id="e2d11-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="e2d11-116">Cómo se asigna la macro de **tipo de notificación** de SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="e2d11-117">Macro OBJECT-TYPE</span><span class="sxs-lookup"><span data-stu-id="e2d11-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="e2d11-118">Cómo se asigna la macro **Object-Type** de SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="e2d11-119">Macro de Convención de texto</span><span class="sxs-lookup"><span data-stu-id="e2d11-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="e2d11-120">Cómo se asigna la macro de **Convención de texto** de SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="e2d11-121">TRAP-TYPE (macro)</span><span class="sxs-lookup"><span data-stu-id="e2d11-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="e2d11-122">Cómo se asigna la macro **Trap-Type** de SNMP a WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="e2d11-123">El proveedor SNMP incluye un compilador que traduce los objetos MIB en objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="e2d11-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="e2d11-124">El compilador SNMP también puede generar errores u otros mensajes.</span><span class="sxs-lookup"><span data-stu-id="e2d11-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="e2d11-125">Para obtener más información, vea [mensajes de error del compilador SNMP](snmp-compiler-error-messages.md) y [mensajes de información general](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e2d11-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2d11-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2d11-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d11-127">Referencia de WMI</span><span class="sxs-lookup"><span data-stu-id="e2d11-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="e2d11-128">Proveedores WMI</span><span class="sxs-lookup"><span data-stu-id="e2d11-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



