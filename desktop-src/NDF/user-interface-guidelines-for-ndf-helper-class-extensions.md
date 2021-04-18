---
title: Directrices de la interfaz de usuario para las extensiones de clase auxiliar NDF
description: Al compilar la clase auxiliar, tendrá que crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104358455"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="687ee-103">Directrices de la interfaz de usuario para las extensiones de clase auxiliar NDF</span><span class="sxs-lookup"><span data-stu-id="687ee-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="687ee-104">Al compilar la clase auxiliar, tendrá que crear texto para ayudar al usuario a comprender la causa de un incidente y los posibles pasos de reparación que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="687ee-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="687ee-105">Causa raíz y reparación</span><span class="sxs-lookup"><span data-stu-id="687ee-105">Root Cause and Repair</span></span>

<span data-ttu-id="687ee-106">Cuando se produce un incidente, aparecerá un cuadro de diálogo para informar al usuario sobre lo que ha sucedido.</span><span class="sxs-lookup"><span data-stu-id="687ee-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="687ee-107">El texto que cree aparecerá en dos áreas independientes.</span><span class="sxs-lookup"><span data-stu-id="687ee-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="687ee-108">**Causa principal**: una breve descripción de la causa del problema.</span><span class="sxs-lookup"><span data-stu-id="687ee-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="687ee-109">Contiene información para ayudar a un administrador o a un usuario avanzado a solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="687ee-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="687ee-110">**Reparación**: amplía la causa raíz para proporcionar más detalles sobre los pasos que puede llevar a cabo un usuario, sin que sea demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="687ee-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="687ee-111">Cada causa o reparación raíz debe tener un título y una descripción.</span><span class="sxs-lookup"><span data-stu-id="687ee-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="687ee-112">Se usará todo el texto antes del primer \\ carácter "n" para el título.</span><span class="sxs-lookup"><span data-stu-id="687ee-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="687ee-113">Todo el texto que sigue al primer \\ carácter "n" (incluidos los saltos de línea posteriores) se utilizará para la descripción.</span><span class="sxs-lookup"><span data-stu-id="687ee-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="687ee-114">Instrucciones de título</span><span class="sxs-lookup"><span data-stu-id="687ee-114">Title Guidelines</span></span>

<span data-ttu-id="687ee-115">El título de una causa o reparación raíz debe seguir estas instrucciones:</span><span class="sxs-lookup"><span data-stu-id="687ee-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="687ee-116">Debe tener 128 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="687ee-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="687ee-117">(se recomiendan 40 caracteres o menos).</span><span class="sxs-lookup"><span data-stu-id="687ee-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="687ee-118">No debe terminar con un punto.</span><span class="sxs-lookup"><span data-stu-id="687ee-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="687ee-119">Instrucciones de Descripción</span><span class="sxs-lookup"><span data-stu-id="687ee-119">Description Guidelines</span></span>

<span data-ttu-id="687ee-120">La descripción de una causa o reparación raíz debe seguir estas directrices:</span><span class="sxs-lookup"><span data-stu-id="687ee-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="687ee-121">Debe tener 512 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="687ee-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="687ee-122">Cada oración debe terminar con un punto.</span><span class="sxs-lookup"><span data-stu-id="687ee-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="687ee-123">El \\ carácter "n" se puede usar para crear un salto de línea en la descripción.</span><span class="sxs-lookup"><span data-stu-id="687ee-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




