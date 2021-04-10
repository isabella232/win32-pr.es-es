---
description: La estructura COMMCONFIG define la configuración de un recurso de comunicaciones, en serie o de otro tipo.
ms.assetid: 05094b98-4694-42dd-883c-b3c90735b3bc
title: Configuración de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6d19bb8478590c85c9f0c1d60ce91cbd1b802a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153096"
---
# <a name="communications-resource-configuration"></a><span data-ttu-id="c1cd3-103">Configuración de recursos de comunicaciones</span><span class="sxs-lookup"><span data-stu-id="c1cd3-103">Communications Resource Configuration</span></span>

<span data-ttu-id="c1cd3-104">La estructura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) define la configuración de un recurso de comunicaciones, en serie o de otro tipo.</span><span class="sxs-lookup"><span data-stu-id="c1cd3-104">The [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure defines the configuration of a communications resource, serial or otherwise.</span></span> <span data-ttu-id="c1cd3-105">El formato de la estructura varía en función del tipo de recurso de comunicaciones (el subtipo de proveedor).</span><span class="sxs-lookup"><span data-stu-id="c1cd3-105">The format of the structure varies depending on the type of communications resource (the provider subtype).</span></span> <span data-ttu-id="c1cd3-106">Los primeros miembros de la estructura son comunes a todos los recursos de comunicaciones; los miembros adicionales se definen para los subtipos específicos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c1cd3-106">The first few structure members are common to all communications resources; additional members are defined for specific provider subtypes.</span></span> <span data-ttu-id="c1cd3-107">Los proveedores de servicios concretos también pueden extender la estructura **COMMCONFIG** .</span><span class="sxs-lookup"><span data-stu-id="c1cd3-107">Specific service providers may extend the **COMMCONFIG** structure as well.</span></span>

<span data-ttu-id="c1cd3-108">Una aplicación puede obtener y establecer la configuración de un recurso de comunicaciones mediante las funciones [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) y [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) .</span><span class="sxs-lookup"><span data-stu-id="c1cd3-108">An application can get and set the configuration of a communications resource by using the [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) and [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) functions.</span></span> <span data-ttu-id="c1cd3-109">Cuando se abre, se inicializa un recurso de comunicaciones con la configuración predeterminada de su subtipo de proveedor.</span><span class="sxs-lookup"><span data-stu-id="c1cd3-109">When opened, a communications resource is initialized using the default configuration for its provider subtype.</span></span> <span data-ttu-id="c1cd3-110">Para obtener y establecer la configuración predeterminada para un subtipo de proveedor, use las funciones [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) y [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) .</span><span class="sxs-lookup"><span data-stu-id="c1cd3-110">To get and set the default configuration for a provider subtype, use the [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga) and [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga) functions.</span></span>

<span data-ttu-id="c1cd3-111">Para solicitar al usuario información de configuración, utilice la función [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) .</span><span class="sxs-lookup"><span data-stu-id="c1cd3-111">To prompt the user for configuration information, use the [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga) function.</span></span> <span data-ttu-id="c1cd3-112">Esta función muestra un cuadro de diálogo definido por el proveedor de servicios y rellena una estructura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) en función de los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="c1cd3-112">This function displays a dialog box defined by the service provider and fills in a [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) structure based on user input.</span></span>

 

 



