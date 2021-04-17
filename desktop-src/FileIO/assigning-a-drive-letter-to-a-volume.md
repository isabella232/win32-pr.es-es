---
description: 'Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función SetVolumeMountPoint, siempre que no haya ningún volumen ya asignado a esa letra de unidad).'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Asignación de una letra de unidad a un volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687287"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="04c12-103">Asignación de una letra de unidad a un volumen</span><span class="sxs-lookup"><span data-stu-id="04c12-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="04c12-104">Puede asignar una letra de unidad (por ejemplo, X: \) a un volumen local mediante la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , siempre que no haya ningún volumen ya asignado a esa letra de unidad).</span><span class="sxs-lookup"><span data-stu-id="04c12-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="04c12-105">Si el volumen local ya tiene una letra de unidad.</span><span class="sxs-lookup"><span data-stu-id="04c12-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="04c12-106">a continuación, se producirá un error en [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) .</span><span class="sxs-lookup"><span data-stu-id="04c12-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="04c12-107">Para controlar esto, elimine primero la letra de unidad mediante la función [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="04c12-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="04c12-108">Para ver un ejemplo de código, consulte [edición de asignaciones de letra de unidad](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="04c12-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="04c12-109">El sistema admite como máximo una letra de unidad por volumen.</span><span class="sxs-lookup"><span data-stu-id="04c12-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="04c12-110">Por lo tanto, no puede tener C: \\ y F: \\ representar el mismo volumen.</span><span class="sxs-lookup"><span data-stu-id="04c12-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="04c12-111">La eliminación de una letra de unidad existente y la asignación de una nueva puede romper las rutas existentes, como las de los accesos directos del escritorio.</span><span class="sxs-lookup"><span data-stu-id="04c12-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="04c12-112">También puede interrumpir la ruta de acceso al programa que realiza la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="04c12-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="04c12-113">Con la administración de la memoria virtual de Windows, esto puede interrumpir la aplicación, lo que deja el sistema en un estado inestable y posiblemente inutilizable.</span><span class="sxs-lookup"><span data-stu-id="04c12-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="04c12-114">Es responsabilidad del diseñador de programas evitar tales posibles catástrofes.</span><span class="sxs-lookup"><span data-stu-id="04c12-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



