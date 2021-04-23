---
description: La clase FOURCCMap proporciona conversión entre subtipos de medios GUID y etiquetas multimedia fourcc de 32 bits de estilo antiguo.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap (clase)
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
ms.openlocfilehash: b9254986bebadeffafaa832817f59194bfc58e12
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908863"
---
# <a name="fourccmap-class"></a><span data-ttu-id="86030-103">FOURCCMap (clase)</span><span class="sxs-lookup"><span data-stu-id="86030-103">FOURCCMap class</span></span>

![jerarquía de clases fourccmap](images/fourcc01.png)

<span data-ttu-id="86030-105">La **clase FOURCCMap proporciona** la conversión entre subtipos de medios **GUID** y etiquetas multimedia **fourcc** de 32 bits de estilo antiguo.</span><span class="sxs-lookup"><span data-stu-id="86030-105">The **FOURCCMap** class provides conversion between **GUID** media subtypes and old-style **FOURCC** 32-bit media tags.</span></span> <span data-ttu-id="86030-106">En las API multimedia originales de Windows, los tipos multimedia se etiquetaban con valores de 32 bits creados a partir de cuatro caracteres de 8 bits y se conocían **como FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="86030-106">In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as **FOURCC** s.</span></span> <span data-ttu-id="86030-107">Los tipos de medios de DirectShow tienen **GUID** para el subtipo, en parte porque son más fáciles de crear (la creación de un **nuevo FOURCC** requiere su registro con Microsoft).</span><span class="sxs-lookup"><span data-stu-id="86030-107">DirectShow media types have **GUID** s for the subtype, partly because these are simpler to create (creation of a new **FOURCC** requires its registration with Microsoft).</span></span> <span data-ttu-id="86030-108">Dado **que los FOURCC** son únicos, se ha hecho posible una asignación uno a uno mediante la asignación de un intervalo de 4000 millones **de GUID** que representan **FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="86030-108">Because **FOURCC** s are unique, a one-to-one mapping has been made possible by allocating a range of 4,000 million **GUID** s representing **FOURCC** s.</span></span> <span data-ttu-id="86030-109">Este intervalo tiene todos **los GUID** del formulario:</span><span class="sxs-lookup"><span data-stu-id="86030-109">This range is all **GUID** s of the form:</span></span>

`XXXXXXXX-0000-0010-8000-00AA00389B71`

<span data-ttu-id="86030-110">Esta clase simplifica la conversión entre **GUID** y **FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="86030-110">This class simplifies conversion between **GUID** s and **FOURCC** s.</span></span> <span data-ttu-id="86030-111">Esto es solo por compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="86030-111">This is for compatibility only.</span></span> <span data-ttu-id="86030-112">Se recomienda que todos los nuevos subtipos multimedia se represente mediante **GUID** creados por Guidgen.exe o una herramienta similar, y no mediante la asignación **de FOURCC** s.</span><span class="sxs-lookup"><span data-stu-id="86030-112">It is recommended that all new media subtypes be represented by **GUID** s created by Guidgen.exe or a similar tool, and not by mapping **FOURCC** s.</span></span>

<span data-ttu-id="86030-113">El objeto se deriva de un **GUID**, sin miembros de datos adicionales, y se puede convertir a un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="86030-113">The object is derived from a **GUID**, with no extra data members, and can be cast to a **GUID**.</span></span> <span data-ttu-id="86030-114">Se puede pasar un **FOURCC al** objeto en tiempo de construcción.</span><span class="sxs-lookup"><span data-stu-id="86030-114">The object can be passed a **FOURCC** at construction time.</span></span> <span data-ttu-id="86030-115">El constructor predeterminado inicializará **fourcc** en cero.</span><span class="sxs-lookup"><span data-stu-id="86030-115">The default constructor will initialize the **FOURCC** to zero.</span></span>

<span data-ttu-id="86030-116">Los [**métodos GetFOURCC**](fourccmap-getfourcc.md) y [**SetFOURCC**](fourccmap-setfourcc.md) no comprueban que las partes fijas del **GUID** se correspondan con **el intervalo FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="86030-116">The [**GetFOURCC**](fourccmap-getfourcc.md) and [**SetFOURCC**](fourccmap-setfourcc.md) methods do not check that the fixed portions of the **GUID** correspond to the **FOURCC** range.</span></span> <span data-ttu-id="86030-117">Por lo tanto, si convierte un puntero a un **GUID** en un puntero a **un FOURCC** y, a continuación, establece u obtiene el **campo FOURCC,** también debe comprobar por separado que el **GUID** está dentro del **intervalo FOURCC.**</span><span class="sxs-lookup"><span data-stu-id="86030-117">Thus, if you cast a pointer to a **GUID** into a pointer to a **FOURCC** and then set or get the **FOURCC** field, you also need to check separately that the **GUID** is within the **FOURCC** range.</span></span>

## <a name="member-functions"></a><span data-ttu-id="86030-118">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="86030-118">Member Functions</span></span>



| <span data-ttu-id="86030-119">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="86030-119">Label</span></span> | <span data-ttu-id="86030-120">Value</span><span class="sxs-lookup"><span data-stu-id="86030-120">Value</span></span> |
|------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="86030-121">**FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="86030-121">**FOURCCMap**</span></span>](fourccmap-fourccmap.md) | <span data-ttu-id="86030-122">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="86030-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="86030-123">**GetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="86030-123">**GetFOURCC**</span></span>](fourccmap-getfourcc.md) | <span data-ttu-id="86030-124">Recupera el **FOURCC de** un **objeto FOURCCMap.**</span><span class="sxs-lookup"><span data-stu-id="86030-124">Retrieves the **FOURCC** from a **FOURCCMap** object.</span></span>    |
| [<span data-ttu-id="86030-125">**SetFOURCC**</span><span class="sxs-lookup"><span data-stu-id="86030-125">**SetFOURCC**</span></span>](fourccmap-setfourcc.md) | <span data-ttu-id="86030-126">Establece la **parte FOURCC** del **objeto FOURCCMap.**</span><span class="sxs-lookup"><span data-stu-id="86030-126">Sets the **FOURCC** portion of the **FOURCCMap** object.</span></span> |



 

 

 



