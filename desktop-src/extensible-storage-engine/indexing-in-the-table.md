---
description: 'Más información sobre: indexación en la tabla'
title: Indexación en la tabla
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082245"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="dcf60-103">Indexación en la tabla</span><span class="sxs-lookup"><span data-stu-id="dcf60-103">Indexing in the Table</span></span>


<span data-ttu-id="dcf60-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="dcf60-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="dcf60-105">Indexación en la tabla</span><span class="sxs-lookup"><span data-stu-id="dcf60-105">Indexing in the Table</span></span>

<span data-ttu-id="dcf60-106">Un índice es un conjunto de columnas de clave que definen un orden persistente de los registros de una tabla.</span><span class="sxs-lookup"><span data-stu-id="dcf60-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="dcf60-107">Los registros son entradas de índice en el índice principal.</span><span class="sxs-lookup"><span data-stu-id="dcf60-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="dcf60-108">Se pueden definir un índice principal y varios índices secundarios para crear pedidos de datos diferentes en la tabla.</span><span class="sxs-lookup"><span data-stu-id="dcf60-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="dcf60-109">Aunque se pueden definir varios índices, los registros se almacenan físicamente en árboles B + en el orden especificado por el índice principal.</span><span class="sxs-lookup"><span data-stu-id="dcf60-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="dcf60-110">El índice principal siempre es un índice clúster y también debe ser único.</span><span class="sxs-lookup"><span data-stu-id="dcf60-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="dcf60-111">El índice principal debe declararse antes de la primera actualización de la tabla para conservar la ordenación del índice.</span><span class="sxs-lookup"><span data-stu-id="dcf60-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="dcf60-112">Cuando la aplicación no define ningún índice principal, los datos se almacenan en el orden en que se agregan los registros a la tabla.</span><span class="sxs-lookup"><span data-stu-id="dcf60-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="dcf60-113">Este índice especial se conoce como índice secuencial.</span><span class="sxs-lookup"><span data-stu-id="dcf60-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="dcf60-114">Los árboles B + independientes se usan para ordenar los registros según el índice secundario.</span><span class="sxs-lookup"><span data-stu-id="dcf60-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="dcf60-115">Las entradas de índice del índice secundario contienen punteros a los datos almacenados según el índice principal.</span><span class="sxs-lookup"><span data-stu-id="dcf60-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="dcf60-116">Las entradas de índice de los registros del índice principal deben ser únicas porque el índice secundario apunta al registro mediante la clave principal del registro.</span><span class="sxs-lookup"><span data-stu-id="dcf60-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="dcf60-117">Los índices secundarios pueden tener o no una restricción de unicidad.</span><span class="sxs-lookup"><span data-stu-id="dcf60-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="dcf60-118">Para obtener más información, vea el tema [información general sobre bases de datos](./database-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf60-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
