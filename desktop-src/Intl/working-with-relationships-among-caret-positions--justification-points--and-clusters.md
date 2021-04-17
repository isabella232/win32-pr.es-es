---
description: En la tabla siguiente se muestran los distintos métodos que la aplicación puede utilizar para controlar el símbolo de intercalación, la justificación y los clústeres.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686814"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="bf58a-103">Trabajar con relaciones entre posiciones del símbolo de intercalación, puntos de justificación y clústeres</span><span class="sxs-lookup"><span data-stu-id="bf58a-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="bf58a-104">En la tabla siguiente se muestran los distintos métodos que la aplicación puede utilizar para controlar el símbolo de intercalación, la justificación y los clústeres.</span><span class="sxs-lookup"><span data-stu-id="bf58a-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="bf58a-105">Tarea</span><span class="sxs-lookup"><span data-stu-id="bf58a-105">Task</span></span>                             | <span data-ttu-id="bf58a-106">Compatibilidad con Uniscribe</span><span class="sxs-lookup"><span data-stu-id="bf58a-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf58a-107">Símbolo de intercalación movimiento por clúster de caracteres</span><span class="sxs-lookup"><span data-stu-id="bf58a-107">Caret move by character cluster</span></span>  | <span data-ttu-id="bf58a-108">El parámetro *pwLogClust* del miembro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** de la estructura [**\_ VISATTR del script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .</span><span class="sxs-lookup"><span data-stu-id="bf58a-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="bf58a-109">El miembro **fCharStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="bf58a-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="bf58a-110">Salto de línea entre caracteres</span><span class="sxs-lookup"><span data-stu-id="bf58a-110">Line breaking between characters</span></span> | <span data-ttu-id="bf58a-111">El parámetro *pwLogClust* del miembro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** de la estructura [**\_ VISATTR del script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .</span><span class="sxs-lookup"><span data-stu-id="bf58a-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="bf58a-112">El miembro **fCharStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="bf58a-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="bf58a-113">Movimiento de intercalación por palabra</span><span class="sxs-lookup"><span data-stu-id="bf58a-113">Caret move by word</span></span>               | <span data-ttu-id="bf58a-114">El miembro **fWordStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="bf58a-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="bf58a-115">División de líneas entre palabras</span><span class="sxs-lookup"><span data-stu-id="bf58a-115">Line breaking between words</span></span>      | <span data-ttu-id="bf58a-116">El miembro **fWordStop** de la [**estructura \_ LOGATTR de script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="bf58a-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="bf58a-117">Justificación</span><span class="sxs-lookup"><span data-stu-id="bf58a-117">Justification</span></span>                    | <span data-ttu-id="bf58a-118">El miembro **uJustification** de la [**estructura \_ VISATTR de script**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="bf58a-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="bf58a-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf58a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf58a-120">Usar Uniscribe</span><span class="sxs-lookup"><span data-stu-id="bf58a-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




