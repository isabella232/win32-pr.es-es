---
description: El enrutador de varios proveedores (MPR) llama a NPGetCaps para averiguar cuándo se iniciarán los proveedores de red (nIndex se establece en WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Reemplazar el intervalo de tiempo de espera predeterminado de MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002548"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="15651-103">Reemplazar el intervalo de tiempo de espera predeterminado de MPR</span><span class="sxs-lookup"><span data-stu-id="15651-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="15651-104">El [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) llama a [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) para averiguar cuándo se iniciarán los proveedores de red (*NINDEX* se establece en WNNC \_ Start).</span><span class="sxs-lookup"><span data-stu-id="15651-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="15651-105">A continuación, el MPR espera el período de tiempo de espera más largo especificado por todos los proveedores de red antes de presentar la red consolidada al usuario.</span><span class="sxs-lookup"><span data-stu-id="15651-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="15651-106">Si uno de los proveedores de red no sabe cuándo se iniciará, MPR usará un tiempo de espera predeterminado de 60 segundos para ese proveedor.</span><span class="sxs-lookup"><span data-stu-id="15651-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="15651-107">Si es necesario, el administrador puede invalidar el tiempo de espera predeterminado creando el siguiente tiempo de espera del registro de **reg \_ DWORD** , donde *n* es el intervalo de tiempo de espera en milisegundos:</span><span class="sxs-lookup"><span data-stu-id="15651-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="15651-108">**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="15651-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="15651-109">En el siguiente pseudocódigo se muestra el flujo de lógica completo para el control de tiempo de espera del MPR.</span><span class="sxs-lookup"><span data-stu-id="15651-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
