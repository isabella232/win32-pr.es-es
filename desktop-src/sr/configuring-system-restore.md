---
title: Configuración de restaurar sistema
description: Restaurar sistema utiliza Instrumental de administración de Windows (WMI) para proporcionar una forma de configurar y usar su funcionalidad con scripts. Expone dos clases, SystemRestore y SystemRestoreConfig, en el \\ espacio de nombres predeterminado raíz.
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323f75cd80f7838e643922d8b9ffa7bf2b121945
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420953"
---
# <a name="configuring-system-restore"></a><span data-ttu-id="9c761-104">Configuración de restaurar sistema</span><span class="sxs-lookup"><span data-stu-id="9c761-104">Configuring System Restore</span></span>

<span data-ttu-id="9c761-105">Restaurar sistema utiliza [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page) (WMI) para proporcionar una forma de configurar y usar su funcionalidad con scripts.</span><span class="sxs-lookup"><span data-stu-id="9c761-105">System Restore uses [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) to provide a scriptable way of configuring and using its functionality.</span></span> <span data-ttu-id="9c761-106">Expone dos clases, [**SystemRestore**](systemrestore.md) y [**SystemRestoreConfig**](systemrestoreconfig.md), en el \\ espacio de nombres predeterminado raíz.</span><span class="sxs-lookup"><span data-stu-id="9c761-106">It exposes two classes, [**SystemRestore**](systemrestore.md) and [**SystemRestoreConfig**](systemrestoreconfig.md), in the root\\default namespace.</span></span>

<span data-ttu-id="9c761-107">La clase [**SystemRestore**](systemrestore.md) proporciona métodos para las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9c761-107">The [**SystemRestore**](systemrestore.md) class provides methods for the following tasks:</span></span>

-   <span data-ttu-id="9c761-108">Deshabilitación y habilitación de la supervisión</span><span class="sxs-lookup"><span data-stu-id="9c761-108">Disabling and enabling monitoring</span></span>
-   <span data-ttu-id="9c761-109">Enumerar los puntos de restauración disponibles</span><span class="sxs-lookup"><span data-stu-id="9c761-109">Listing available restore points</span></span>
-   <span data-ttu-id="9c761-110">Iniciar una restauración en el sistema local</span><span class="sxs-lookup"><span data-stu-id="9c761-110">Initiating a restore on the local system</span></span>
-   <span data-ttu-id="9c761-111">Recuperar el estado de la última restauración del sistema</span><span class="sxs-lookup"><span data-stu-id="9c761-111">Retrieving the status of the last system restore</span></span>

<span data-ttu-id="9c761-112">La clase [**SystemRestoreConfig**](systemrestoreconfig.md) proporciona propiedades para controlar la frecuencia de creación de puntos de restauración programados y la cantidad de espacio en disco consumido por restaurar sistema en cada unidad.</span><span class="sxs-lookup"><span data-stu-id="9c761-112">The [**SystemRestoreConfig**](systemrestoreconfig.md) class provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed by System Restore on each drive.</span></span>

<span data-ttu-id="9c761-113">Se puede tener acceso a ambas clases de forma remota mediante técnicas WMI estándar.</span><span class="sxs-lookup"><span data-stu-id="9c761-113">Both classes can be accessed remotely using standard WMI techniques.</span></span> <span data-ttu-id="9c761-114">Para obtener una descripción completa de WMI, consulte [instrumental de administración de Windows](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="9c761-114">For a complete description of WMI, see [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

 

 