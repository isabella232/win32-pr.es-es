---
description: Una regla de negocio permite a una aplicación usar la lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Reglas de negocios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279636"
---
# <a name="business-rules"></a><span data-ttu-id="0761f-103">Reglas de negocios</span><span class="sxs-lookup"><span data-stu-id="0761f-103">Business Rules</span></span>

<span data-ttu-id="0761f-104">Una regla de negocio permite a una aplicación usar la lógica en tiempo de ejecución para calificar los permisos concedidos al cliente.</span><span class="sxs-lookup"><span data-stu-id="0761f-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="0761f-105">Una regla de negocios es un script escrito en el lenguaje de programación de Visual Basic Scripting Edition (VBScript) o escrito mediante el software de desarrollo de Microsoft JScript que está asociado a un objeto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="0761f-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="0761f-106">Cuando una aplicación comprueba el acceso para una operación, el administrador de autorización comprueba primero si el cliente actual tiene acceso a las tareas que contienen esa operación pero que no están asociadas con las reglas de negocios.</span><span class="sxs-lookup"><span data-stu-id="0761f-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="0761f-107">Si no se concede el acceso de esta manera, el administrador de autorización ejecuta scripts de reglas de negocios asociados a cualquier tarea que contenga la operación.</span><span class="sxs-lookup"><span data-stu-id="0761f-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="0761f-108">Una aplicación pasa información a un script de regla de negocio como un par de matrices que representan los nombres y valores de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="0761f-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="0761f-109">El script tiene acceso a estos parámetros a través de un objeto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) que se crea cuando se ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="0761f-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="0761f-110">Un script de regla de negocio no se puede asignar a una tarea contenida por un ámbito delegado.</span><span class="sxs-lookup"><span data-stu-id="0761f-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0761f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0761f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0761f-112">Calificar el acceso con la lógica de negocios en C++</span><span class="sxs-lookup"><span data-stu-id="0761f-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



