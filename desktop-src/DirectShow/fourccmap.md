---
description: La clase FOURCCMap proporciona conversión entre subtipos de medios GUID y etiquetas de medios de 32 bits FOURCC de estilo antiguo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Clase FOURCCMap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152346"
---
# <a name="fourccmap-class"></a><span data-ttu-id="95f56-103">Clase FOURCCMap</span><span class="sxs-lookup"><span data-stu-id="95f56-103">FOURCCMap class</span></span>

![jerarquía de clases fourccmap](images/fourcc01.png)

<span data-ttu-id="95f56-105">La clase **FOURCCMap** proporciona conversión entre subtipos de medios **GUID** y etiquetas de medios de 32 bits **FourCC** de estilo antiguo.</span><span class="sxs-lookup"><span data-stu-id="95f56-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="95f56-106">En las API multimedia originales de Windows, los tipos de medios se etiquetaron con valores de 32 bits creados a partir de caracteres de 4 8 bits y se conocían como **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="95f56-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="95f56-107">Los tipos de medios de DirectShow tienen **GUID** s para el subtipo, en parte porque son más fáciles de crear (la creación de un nuevo **FourCC** requiere su registro en Microsoft).</span><span class="sxs-lookup"><span data-stu-id="95f56-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="95f56-108">Dado que los **FourCC** son únicos, se ha hecho una asignación uno a uno asignando un intervalo de 4 mil millones **GUID** que representan los **FourCC**.</span><span class="sxs-lookup"><span data-stu-id="95f56-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="95f56-109">Este intervalo son todos los **GUID** del formulario:</span><span class="sxs-lookup"><span data-stu-id="95f56-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="95f56-110">Esta clase simplifica la conversión entre **GUID** s y **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="95f56-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="95f56-111">Esto es solo por compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="95f56-111">This is for compatibility only.</span></span> <span data-ttu-id="95f56-112">Se recomienda que todos los subtipos de medios nuevos estén representados por **GUID** s creados por Guidgen.exe o una herramienta similar, y no por la asignación de **FourCC** s.</span><span class="sxs-lookup"><span data-stu-id="95f56-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="95f56-113">El objeto se deriva de un **GUID**, sin miembros de datos adicionales, y se puede convertir en un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="95f56-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="95f56-114">El objeto se puede pasar a **FourCC** en el momento de la construcción.</span><span class="sxs-lookup"><span data-stu-id="95f56-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="95f56-115">El constructor predeterminado inicializará el **FourCC** en cero.</span><span class="sxs-lookup"><span data-stu-id="95f56-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="95f56-116">Los métodos [**GetFOURCC**](fourccmap-getfourcc.md) y [**SetFOURCC**](fourccmap-setfourcc.md) no comprueban que las partes fijas del **GUID** se correspondan con el intervalo de **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="95f56-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="95f56-117">Por lo tanto, si convierte un puntero en un **GUID** en un puntero a un **FourCC** y, a continuación, establece u obtiene el campo **FourCC** , también debe comprobar por separado que el **GUID** está dentro del intervalo de **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="95f56-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="95f56-118">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="95f56-118">Member Functions</span></span>



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="95f56-119">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="95f56-119">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="95f56-120">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="95f56-120">Constructor method.</span></span>                                      |
| [<span data-ttu-id="95f56-121">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="95f56-121">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="95f56-122">Recupera el **FourCC** de un objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="95f56-122">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="95f56-123">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="95f56-123">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="95f56-124">Establece la parte **FourCC** del objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="95f56-124">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



