---
description: El filtro de direcciones notifica al controlador de Monitor de red para que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificadas (Ethernet, token ring y FDDI).
ms.assetid: 23a38f49-2d63-4fc8-8113-29143493359c
title: Escribir la parte de filtro de ADDRESSTABLE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b06b00d046d555dffc39561b817629f4f47ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669674"
---
# <a name="writing-addresstable-filter-portion"></a><span data-ttu-id="9481a-103">Escribir la parte de filtro de ADDRESSTABLE</span><span class="sxs-lookup"><span data-stu-id="9481a-103">Writing ADDRESSTABLE Filter Portion</span></span>

<span data-ttu-id="9481a-104">El filtro de direcciones notifica al controlador de Monitor de red para que acepte fotogramas que tengan uno de los distintos tipos de direcciones MAC especificadas (Ethernet, token ring y FDDI).</span><span class="sxs-lookup"><span data-stu-id="9481a-104">The address filter notifies the Network Monitor driver to accept frames that have one of a variety of specified MAC address types (Ethernet, Token Ring, and FDDI).</span></span> <span data-ttu-id="9481a-105">Puede especificar un máximo de ocho pares de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9481a-105">You can specify a maximum of eight address pairs.</span></span> <span data-ttu-id="9481a-106">Un par de direcciones puede especificar un origen, un destino, ambos o ninguno.</span><span class="sxs-lookup"><span data-stu-id="9481a-106">An address pair can specify a source, a destination, both, or neither.</span></span>

<span data-ttu-id="9481a-107">La parte de la dirección del filtro consta de dos estructuras: [**ADDRESSTABLE**](addresstable.md) y [**ADDRESSPAIR**](addresspair.md).</span><span class="sxs-lookup"><span data-stu-id="9481a-107">The address portion of the filter consists of two structures: [**ADDRESSTABLE**](addresstable.md) and [**ADDRESSPAIR**](addresspair.md).</span></span>

<span data-ttu-id="9481a-108">Si NO especifica ninguna dirección, todos los marcos pasarán el filtro de direcciones.</span><span class="sxs-lookup"><span data-stu-id="9481a-108">If you specify NO addresses, then ALL frames will pass the address filter.</span></span> <span data-ttu-id="9481a-109">Sin embargo, si especifica cualquier dirección, solo se pasarán los fotogramas que pasen el filtro de dirección determinado.</span><span class="sxs-lookup"><span data-stu-id="9481a-109">However, if you specify any addresses, only those frames that pass the given address filter will pass.</span></span>

<span data-ttu-id="9481a-110">La creación del filtro de direcciones implica la asignación de una estructura [**ADDRESSTABLE**](addresstable.md) y el rellenado de miembros de la estructura [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="9481a-110">Building the address filter involves allocating an [**ADDRESSTABLE**](addresstable.md) structure and filling in members of the [**ADDRESSPAIR**](addresspair.md) structure.</span></span>

<span data-ttu-id="9481a-111">**Para compilar la parte de la dirección de un filtro de captura**</span><span class="sxs-lookup"><span data-stu-id="9481a-111">**To build the address portion of a capture filter**</span></span>

1.  <span data-ttu-id="9481a-112">Use la marca **CAPTUREFILTER \_ Flags \_ local \_ Only** de la estructura [**CAPTUREFILTER**](capturefilter.md) para restringir la captura al tráfico hacia y desde el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9481a-112">Use the **CAPTUREFILTER\_FLAGS\_LOCAL\_ONLY** flag of the [**CAPTUREFILTER**](capturefilter.md) structure to restrict the capture to traffic to and from your local computer.</span></span>

    <span data-ttu-id="9481a-113">Al establecer esta marca, no se establecerá la NIC en el modo promiscuo; el archivo de captura solo capturará el tráfico local.</span><span class="sxs-lookup"><span data-stu-id="9481a-113">Setting this flag will not set the NIC to promiscuous mode; the capture file will capture only local traffic.</span></span>

2.  <span data-ttu-id="9481a-114">Use el código de ejemplo siguiente para definir la estructura [**ADDRESSTABLE**](addresstable.md) :</span><span class="sxs-lookup"><span data-stu-id="9481a-114">Use the following example code to define the [**ADDRESSTABLE**](addresstable.md) structure:</span></span>

    ``` syntax
    typedef struct _ADDRESSTABLE
    {
        DWORD           nAddressPairs;
        DWORD           nNonMacAddressPairs;
        ADDRESSPAIR     AddressPair[MAX_ADDRESS_PAIRS];
    } ADDRESSTABLE;

    typedef ADDRESSTABLE *LPADDRESSTABLE;
     
    typedef struct _ADDRESSPAIR
    {
        WORD        AddressFlags;
        WORD        NalReserved;
        ADDRESS     DstAddress;
        ADDRESS     SrcAddress;
    } ADDRESSPAIR;

    typedef ADDRESSPAIR *LPADDRESSPAIR;
    ```

3.  <span data-ttu-id="9481a-115">Utilice la información que se muestra en la tabla siguiente para seleccionar un tipo de marca [**ADDRESSPAIR**](addresspair.md) .</span><span class="sxs-lookup"><span data-stu-id="9481a-115">Use the information, listed in the following table, to select an [**ADDRESSPAIR**](addresspair.md) flag type.</span></span> 

    | <span data-ttu-id="9481a-116">Marca</span><span class="sxs-lookup"><span data-stu-id="9481a-116">Flag</span></span>                             | <span data-ttu-id="9481a-117">Significado</span><span class="sxs-lookup"><span data-stu-id="9481a-117">Meaning</span></span>                                                                               |
    |----------------------------------|---------------------------------------------------------------------------------------|
    | <span data-ttu-id="9481a-118">marcas de dirección \_ \_ Match \_ DST</span><span class="sxs-lookup"><span data-stu-id="9481a-118">ADDRESS\_FLAGS\_MATCH\_DST</span></span>       | <span data-ttu-id="9481a-119">Coincide con una dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="9481a-119">Matches a destination address.</span></span>                                                        |
    | <span data-ttu-id="9481a-120">coincidencia de marcas de dirección \_ \_ \_ src</span><span class="sxs-lookup"><span data-stu-id="9481a-120">ADDRESS\_FLAGS\_MATCH\_SRC</span></span>       | <span data-ttu-id="9481a-121">Coincide con una dirección de origen</span><span class="sxs-lookup"><span data-stu-id="9481a-121">Matches a source address</span></span>                                                              |
    | <span data-ttu-id="9481a-122">\_excluir marcas de dirección \_</span><span class="sxs-lookup"><span data-stu-id="9481a-122">ADDRESS\_FLAGS\_EXCLUDE</span></span>          | <span data-ttu-id="9481a-123">Excluye el marco si se encuentra esta dirección (ya sea un origen o un destino definidos).</span><span class="sxs-lookup"><span data-stu-id="9481a-123">Excludes the frame if this address is found (either a defined source or destination).</span></span> |
    | <span data-ttu-id="9481a-124">marcas de dirección \_ \_ grupo de DST \_ \_</span><span class="sxs-lookup"><span data-stu-id="9481a-124">ADDRESS\_FLAGS\_DST\_GROUP\_ADDR</span></span> | <span data-ttu-id="9481a-125">Coincide con el bit de grupo (de la dirección de destino) solo para mensajes de tipo difusión.</span><span class="sxs-lookup"><span data-stu-id="9481a-125">Matches group bit (of the destination address) only for broadcast-type messages.</span></span>      |
    | <span data-ttu-id="9481a-126">las \_ marcas de dirección \_ coinciden con \_ ambas</span><span class="sxs-lookup"><span data-stu-id="9481a-126">ADDRESS\_FLAGS\_MATCH\_BOTH</span></span>      | <span data-ttu-id="9481a-127">Coincide con las direcciones de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="9481a-127">Matches both the destination and source addresses.</span></span>                                    |

    

     

4.  <span data-ttu-id="9481a-128">Rellene una dirección de destino, que se evalúa con la marca [**ADDRESSPAIR**](addresspair.md) que seleccione.</span><span class="sxs-lookup"><span data-stu-id="9481a-128">Fill in a destination address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
5.  <span data-ttu-id="9481a-129">Rellene una dirección de origen, que se evalúa con la marca [**ADDRESSPAIR**](addresspair.md) que seleccione.</span><span class="sxs-lookup"><span data-stu-id="9481a-129">Fill in a source address, which is evaluated against the [**ADDRESSPAIR**](addresspair.md) flag that you select.</span></span>
6.  <span data-ttu-id="9481a-130">Rellene la estructura [**ADDRESSTABLE**](addresstable.md) con una matriz de estructuras [**ADDRESSPAIR**](addresspair.md) , que incluye los pares de direcciones que el controlador evalúa.</span><span class="sxs-lookup"><span data-stu-id="9481a-130">Populate the [**ADDRESSTABLE**](addresstable.md) structure with an array of [**ADDRESSPAIR**](addresspair.md) structures, which includes the address pairs that the driver evaluates.</span></span> <span data-ttu-id="9481a-131">Todos los pares de direcciones se evalúan como una instrucción OR lógica (ADDRESSPAIR 1 \| \| ADDRESSPAIR 2).</span><span class="sxs-lookup"><span data-stu-id="9481a-131">All address pairs are evaluated as a logical OR statement (ADDRESSPAIR 1 \|\| ADDRESSPAIR 2).</span></span> <span data-ttu-id="9481a-132">Puede incluir un máximo de ocho pares de direcciones en un filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="9481a-132">You can include a maximum of eight address pairs in a capture filter.</span></span>

 

 



