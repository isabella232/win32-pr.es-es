---
description: Glosario de términos de Monitor de red que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Monitor de red)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082223"
---
# <a name="p-network-monitor"></a><span data-ttu-id="bbdf0-103">P (Monitor de red)</span><span class="sxs-lookup"><span data-stu-id="bbdf0-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="bbdf0-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**paquete**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-105">Consulte [*Frame*](f.md).</span><span class="sxs-lookup"><span data-stu-id="bbdf0-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**Analizador**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-107">Componente que detecta un protocolo específico en una captura retrasada.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="bbdf0-108">Cada analizador puede detectar un protocolo.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="bbdf0-109">Sin embargo, un archivo DLL de analizador puede contener varios analizadores.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="bbdf0-110">También se denomina analizador de protocolos.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-112">Un Monitor de red archivo de inicialización que contiene una lista de todos los analizadores instalados.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="bbdf0-113">Para cada analizador hay una cadena de comentario que describe el analizador, el siguiente conjunto del analizador y cualquier archivo de ayuda asociado con el analizador.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="bbdf0-114">El archivo INI del analizador se actualiza cuando Monitor de red llama a **ParserAutoInstallInfo**, o cuando el dll del analizador llama a **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Contador**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-116">Herramienta de software que le permite ver las variables relacionadas con el rendimiento de la red que identifican la actividad de un proceso.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**modo promiscuo**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-118">Estado en el que una tarjeta adaptadora de red copia todos los fotogramas que pasan a través de la red, independientemente de la dirección de destino a un búfer local.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="bbdf0-119">Este modo permite a Monitor de red capturar y mostrar todo el tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**propiedad**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-121">Un elemento Protocol en un analizador que describe un campo de datos dentro de un marco que se envía mediante ese protocolo.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**base de datos de propiedades**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-123">Base de datos interna que define todas las propiedades que admite un protocolo concreto.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="bbdf0-124">La base de datos de propiedades contiene una estructura **PROPERTYINFO** para cada propiedad que define el analizador.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="bbdf0-125">Monitor de red usa la información de la base de datos cuando adjunta una definición de propiedad a una instancia de la propiedad y cuando da formato a los datos de propiedad que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="bbdf0-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**nivel de protocolo**</span><span class="sxs-lookup"><span data-stu-id="bbdf0-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="bbdf0-127">Agrupación lógica de propiedades de protocolo.</span><span class="sxs-lookup"><span data-stu-id="bbdf0-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



