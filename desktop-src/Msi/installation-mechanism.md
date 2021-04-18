---
description: 'Hay dos fases para un proceso de instalación correcta: adquisición y ejecución. Si la instalación no se realiza correctamente, puede producirse una fase de reversión.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652507"
---
# <a name="installation-mechanism"></a><span data-ttu-id="1d289-104">Mecanismo de instalación</span><span class="sxs-lookup"><span data-stu-id="1d289-104">Installation Mechanism</span></span>

<span data-ttu-id="1d289-105">Hay dos fases para un proceso de instalación correcta: adquisición y ejecución.</span><span class="sxs-lookup"><span data-stu-id="1d289-105">There are two phases to a successful installation process: acquisition and execution.</span></span> <span data-ttu-id="1d289-106">Si la instalación no se realiza correctamente, puede producirse una fase de reversión.</span><span class="sxs-lookup"><span data-stu-id="1d289-106">If the installation is unsuccessful, a rollback phase may occur.</span></span>

## <a name="acquisition"></a><span data-ttu-id="1d289-107">Adquisición</span><span class="sxs-lookup"><span data-stu-id="1d289-107">Acquisition</span></span>

<span data-ttu-id="1d289-108">Al principio de la fase de adquisición, una aplicación o un usuario indica al instalador que instale una característica o una aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d289-108">At the beginning of the acquisition phase, an application or a user instructs the installer to install a feature or an application.</span></span> <span data-ttu-id="1d289-109">A continuación, el instalador progresa a través de las acciones especificadas en las tablas de secuencia de la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="1d289-109">The installer then progresses through the actions specified in the sequence tables of the installation database.</span></span> <span data-ttu-id="1d289-110">Estas acciones consultan la base de datos de instalación y generan un script que proporciona un procedimiento paso a paso para realizar la instalación.</span><span class="sxs-lookup"><span data-stu-id="1d289-110">These actions query the installation database and generate a script that gives a step-by-step procedure for performing the installation.</span></span>

## <a name="execution"></a><span data-ttu-id="1d289-111">Ejecución</span><span class="sxs-lookup"><span data-stu-id="1d289-111">Execution</span></span>

<span data-ttu-id="1d289-112">Durante la fase de ejecución, el instalador pasa la información a un proceso con privilegios elevados y ejecuta el script.</span><span class="sxs-lookup"><span data-stu-id="1d289-112">During the execution phase, the installer passes the information to a process with elevated privileges and runs the script.</span></span>

## <a name="rollback"></a><span data-ttu-id="1d289-113">Reversión</span><span class="sxs-lookup"><span data-stu-id="1d289-113">Rollback</span></span>

<span data-ttu-id="1d289-114">Si una instalación no se realiza correctamente, el programa de instalación restaura el estado original del equipo.</span><span class="sxs-lookup"><span data-stu-id="1d289-114">If an installation is unsuccessful, the installer restores the original state of the computer.</span></span> <span data-ttu-id="1d289-115">Cuando el instalador procesa el script de instalación, genera simultáneamente un script de reversión.</span><span class="sxs-lookup"><span data-stu-id="1d289-115">When the installer processes the installation script it simultaneously generates a rollback script.</span></span> <span data-ttu-id="1d289-116">Además del script de reversión, el instalador guarda una copia de todos los archivos que elimina durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="1d289-116">In addition to the rollback script, the installer saves a copy of every file it deletes during the installation.</span></span> <span data-ttu-id="1d289-117">Estos archivos se conservan en un directorio oculto del sistema.</span><span class="sxs-lookup"><span data-stu-id="1d289-117">These files are kept in a hidden, system directory.</span></span> <span data-ttu-id="1d289-118">Una vez completada la instalación, se eliminan el script de reversión y los archivos guardados.</span><span class="sxs-lookup"><span data-stu-id="1d289-118">Once the installation is complete, the rollback script and the saved files are deleted.</span></span> <span data-ttu-id="1d289-119">Para obtener más información, consulte [reversión de instalación](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="1d289-119">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

 

 



