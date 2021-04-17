---
description: Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierten las cuentas de usuario.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Crear la tabla InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667027"
---
# <a name="authoring-the-installexecutesequence-table"></a><span data-ttu-id="01957-103">Crear la tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="01957-103">Authoring the InstallExecuteSequence Table</span></span>

<span data-ttu-id="01957-104">Las acciones personalizadas ProcessAccounts y UninstallAccounts generan las acciones personalizadas diferidas que crean, quitan o revierten las cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="01957-104">The custom actions ProcessAccounts and UninstallAccounts generate the deferred custom actions that create, remove, or rollback user accounts.</span></span> <span data-ttu-id="01957-105">Las acciones personalizadas ProcessAccounts y UninstallAccounts deben especificarse en la [tabla InstallExecuteSequence](installexecutesequence-table.md) que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="01957-105">The custom actions ProcessAccounts and UninstallAccounts must be entered into the [InstallExecuteSequence table](installexecutesequence-table.md) to be executed.</span></span> <span data-ttu-id="01957-106">Agregue las siguientes entradas a la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="01957-106">Add the following entries to the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="01957-107">Dado que estas acciones personalizadas deben formar parte de la generación del script, ambas acciones personalizadas se deben secuenciar después de la [acción InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="01957-107">Because these custom actions must be a part of the script generation, both custom actions must be sequenced after the [InstallInitialize action](installinitialize-action.md).</span></span>

<span data-ttu-id="01957-108">La condición de ProcessAccounts garantiza lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="01957-108">The condition on ProcessAccounts ensures the following.</span></span> <span data-ttu-id="01957-109">Consulte [Sintaxis de la instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="01957-109">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

-   <span data-ttu-id="01957-110">ProcessAccounts solo se ejecuta si el componente TestAccount se instala localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="01957-110">ProcessAccounts runs only if the component TestAccount is being installed locally on the computer.</span></span>
-   <span data-ttu-id="01957-111">La cuenta de prueba de componentes no está instalada actualmente o está instalada para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="01957-111">The component Test Account is currently not installed or is installed to run from the source.</span></span>

<span data-ttu-id="01957-112">La condición de UninstallAccount garantiza lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="01957-112">The condition on UninstallAccount ensures the following:</span></span>

-   <span data-ttu-id="01957-113">UninstallAccounts solo se ejecuta si el componente TestAccount está instalado localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="01957-113">UninstallAccounts runs only if the component TestAccount is installed locally on the computer.</span></span>
-   <span data-ttu-id="01957-114">La cuenta de prueba de componentes se está quitando o se está instalando para ejecutarse desde el origen.</span><span class="sxs-lookup"><span data-stu-id="01957-114">The component Test Account is being removed or being installed to run from the source.</span></span>

[<span data-ttu-id="01957-115">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="01957-115">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)



| <span data-ttu-id="01957-116">Acción</span><span class="sxs-lookup"><span data-stu-id="01957-116">Action</span></span>            | <span data-ttu-id="01957-117">Condición</span><span class="sxs-lookup"><span data-stu-id="01957-117">Condition</span></span>                                                           | <span data-ttu-id="01957-118">Secuencia</span><span class="sxs-lookup"><span data-stu-id="01957-118">Sequence</span></span> |
|-------------------|---------------------------------------------------------------------|----------|
| <span data-ttu-id="01957-119">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="01957-119">ProcessAccounts</span></span>   | <span data-ttu-id="01957-120">VersionNT y (? TestAccount = 2 o? TestAccount = 4) y $TestAccount = 3</span><span class="sxs-lookup"><span data-stu-id="01957-120">VersionNT AND (?TestAccount=2 OR ?TestAccount=4) AND $TestAccount=3</span></span> | <span data-ttu-id="01957-121">1550</span><span class="sxs-lookup"><span data-stu-id="01957-121">1550</span></span>     |
| <span data-ttu-id="01957-122">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="01957-122">UninstallAccounts</span></span> | <span data-ttu-id="01957-123">VersionNT y? TestAccount = 3 y ($TestAccount = 4 o $TestAccount = 2)</span><span class="sxs-lookup"><span data-stu-id="01957-123">VersionNT AND ?TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2)</span></span> | <span data-ttu-id="01957-124">1560</span><span class="sxs-lookup"><span data-stu-id="01957-124">1560</span></span>     |



 

<span data-ttu-id="01957-125">Continúe con [la creación de la interfaz de usuario para la entrada de contraseña](authoring-the-user-interface-for-password-input.md).</span><span class="sxs-lookup"><span data-stu-id="01957-125">Continue to [Authoring the user interface for password input](authoring-the-user-interface-for-password-input.md).</span></span>

 

 



