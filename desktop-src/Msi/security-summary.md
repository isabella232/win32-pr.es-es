---
description: La propiedad Resumen de seguridad transmite si el paquete debe abrirse como de solo lectura.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Propiedad de Resumen de seguridad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653872"
---
# <a name="security-summary-property"></a><span data-ttu-id="5b2dd-103">Propiedad de Resumen de seguridad</span><span class="sxs-lookup"><span data-stu-id="5b2dd-103">Security Summary property</span></span>

<span data-ttu-id="5b2dd-104">La propiedad **Resumen de seguridad** transmite si el paquete debe abrirse como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-104">The **Security Summary** property conveys whether the package should be opened as read-only.</span></span> <span data-ttu-id="5b2dd-105">La herramienta de edición de bases de datos no debe modificar una base de datos forzada de solo lectura y debe emitir una advertencia en los intentos de modificar una base de datos recomendada de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-105">The database editing tool should not modify a read-only enforced database and should issue a warning at attempts to modify a read-only recommended database.</span></span> <span data-ttu-id="5b2dd-106">Los siguientes valores de esta propiedad se aplican a los archivos Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-106">The following values of this property are applicable to Windows Installer files.</span></span>



| <span data-ttu-id="5b2dd-107">Value</span><span class="sxs-lookup"><span data-stu-id="5b2dd-107">Value</span></span> | <span data-ttu-id="5b2dd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b2dd-108">Description</span></span>           |
|-------|-----------------------|
| <span data-ttu-id="5b2dd-109">0</span><span class="sxs-lookup"><span data-stu-id="5b2dd-109">0</span></span>     | <span data-ttu-id="5b2dd-110">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="5b2dd-110">No restriction</span></span>        |
| <span data-ttu-id="5b2dd-111">2</span><span class="sxs-lookup"><span data-stu-id="5b2dd-111">2</span></span>     | <span data-ttu-id="5b2dd-112">Recomendado solo lectura</span><span class="sxs-lookup"><span data-stu-id="5b2dd-112">Read-only recommended</span></span> |
| <span data-ttu-id="5b2dd-113">4</span><span class="sxs-lookup"><span data-stu-id="5b2dd-113">4</span></span>     | <span data-ttu-id="5b2dd-114">Solo lectura forzada</span><span class="sxs-lookup"><span data-stu-id="5b2dd-114">Read-only enforced</span></span>    |



 

<span data-ttu-id="5b2dd-115">Esta propiedad debe establecerse en solo lectura recomendado (2) para una base de datos de instalación y en la aplicación de solo lectura (4) para una transformación o revisión.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-115">This property should be set to read-only recommended (2) for an installation database and to read-only enforced (4) for a transform or patch.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2dd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b2dd-116">Requirements</span></span>



| <span data-ttu-id="5b2dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2dd-117">Requirement</span></span> | <span data-ttu-id="5b2dd-118">Value</span><span class="sxs-lookup"><span data-stu-id="5b2dd-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2dd-119">Versión</span><span class="sxs-lookup"><span data-stu-id="5b2dd-119">Version</span></span><br/> | <span data-ttu-id="5b2dd-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b2dd-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b2dd-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b2dd-122">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b2dd-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b2dd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b2dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2dd-124">Descripciones de propiedades de Resumen</span><span class="sxs-lookup"><span data-stu-id="5b2dd-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




