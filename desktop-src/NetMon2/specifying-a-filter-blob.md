---
description: Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un BLOB en filtro para omitir las NIC que no le interesan.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Especificación de un BLOB en filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686880"
---
# <a name="specifying-a-filter-blob"></a><span data-ttu-id="990d5-103">Especificación de un BLOB en filtro</span><span class="sxs-lookup"><span data-stu-id="990d5-103">Specifying a Filter BLOB</span></span>

<span data-ttu-id="990d5-104">Al seleccionar una tarjeta de interfaz de red (NIC) registrada en un equipo local, puede usar un [*BLOB en filtro*](f.md) para omitir las NIC que no le interesan.</span><span class="sxs-lookup"><span data-stu-id="990d5-104">When you select a registered network interface card (NIC) listed on a local computer, you can use a [*filter BLOB*](f.md) to disregard the NICs you are not interested in.</span></span> <span data-ttu-id="990d5-105">Por ejemplo, puede restringir la búsqueda de un tipo específico de tarjeta (como ETHERNET) o una dirección MAC específica.</span><span class="sxs-lookup"><span data-stu-id="990d5-105">For example, you could restrict the search for a specific type of card (such as ETHERNET) or a specific MAC address.</span></span>

<span data-ttu-id="990d5-106">Durante la búsqueda de una NIC, cada entrada del BLOB en filtro debe coincidir con una entrada equivalente en el BLOB NPP que representa la NIC.</span><span class="sxs-lookup"><span data-stu-id="990d5-106">During the search for a NIC, every entry in the filter BLOB must match an equivalent entry in the NPP BLOB that represents the NIC.</span></span> <span data-ttu-id="990d5-107">Los blobs de filtro también pueden ser [*blobs especiales*](s.md).</span><span class="sxs-lookup"><span data-stu-id="990d5-107">Filter BLOBs can also be [*special BLOBs*](s.md).</span></span>

<span data-ttu-id="990d5-108">Cuando se llama a la función [**GetNPPBlobFromUI**](getnppblobfromui.md) , el BLOB de filtro restringe las NIC que se muestran en el cuadro de diálogo **seleccionar una red** .</span><span class="sxs-lookup"><span data-stu-id="990d5-108">When the [**GetNPPBlobFromUI**](getnppblobfromui.md) function is called, the filter BLOB restricts the NICs displayed in the **Select a network** dialog box.</span></span> <span data-ttu-id="990d5-109">Cuando se llama a la función [**GetNPPBlobTable**](getnppblobtable.md) , el BLOB de filtro restringe las NIC devueltas en la tabla de blobs.</span><span class="sxs-lookup"><span data-stu-id="990d5-109">When the [**GetNPPBlobTable**](getnppblobtable.md) function is called, the filter BLOB restricts the NICs returned in the BLOB table.</span></span>

<span data-ttu-id="990d5-110">Para usar el filtro, debe crear un BLOB de filtro, establecer los valores de las propiedades que desea filtrar (incluidas las entradas de BLOBs especiales) y, a continuación, especificar el filtro de BLOBs y una llamada a la función [**GetNPPBlobTable**](getnppblobtable.md) o [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="990d5-110">To use the filter, you must create a filter BLOB, set the values of the properties you want to filter on (including any special BLOB entries), and then specify the BLOB filter and a call to the [**GetNPPBlobTable**](getnppblobtable.md) or [**GetNPPBlobFromUI**](getnppblobfromui.md) function.</span></span>



| <span data-ttu-id="990d5-111">Para obtener información acerca de</span><span class="sxs-lookup"><span data-stu-id="990d5-111">For information on</span></span>                                 | <span data-ttu-id="990d5-112">Vea</span><span class="sxs-lookup"><span data-stu-id="990d5-112">See</span></span>                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="990d5-113">Cómo seleccionar una NIC registrada en un equipo local</span><span class="sxs-lookup"><span data-stu-id="990d5-113">How to select a NIC registered on a local computer</span></span> | [<span data-ttu-id="990d5-114">Selección de una NIC registrada</span><span class="sxs-lookup"><span data-stu-id="990d5-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="990d5-115">Recuperación de una tabla BLOB de NPP</span><span class="sxs-lookup"><span data-stu-id="990d5-115">Retrieving an NPP BLOB table</span></span>                       | [<span data-ttu-id="990d5-116">Selección de una NIC de una tabla BLOB NPP devuelta</span><span class="sxs-lookup"><span data-stu-id="990d5-116">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



