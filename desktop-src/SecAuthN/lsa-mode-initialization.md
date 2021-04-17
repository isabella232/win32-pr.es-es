---
description: Cuando se inicia el equipo, la autoridad de seguridad local (LSA) carga automáticamente todos los archivos dll registrados del proveedor de compatibilidad de seguridad (SSP/AP) en su espacio de proceso. En las ilustraciones siguientes se muestra el proceso de inicialización.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Inicialización del modo LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546347"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="4c3a3-104">Inicialización del modo LSA</span><span class="sxs-lookup"><span data-stu-id="4c3a3-104">LSA Mode Initialization</span></span>

<span data-ttu-id="4c3a3-105">Cuando se inicia el equipo, la [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) carga automáticamente todos los archivos DLL del paquete de autenticación del [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) (SSP/AP) registrados en su espacio de proceso.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="4c3a3-106">En las ilustraciones siguientes se muestra el proceso de inicialización.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="4c3a3-107">"Kerberos" representa a Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP y "mi SSP/AP" representa un SSP/AP personalizado que contiene dos paquetes de seguridad personalizados.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![inicialización del modo LSA](images/lsamode1.png)

<span data-ttu-id="4c3a3-109">En el inicio, LSA llama a la función [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) en cada SSP/AP para obtener punteros a las funciones implementadas por cada [*paquete de seguridad*](../secgloss/s-gly.md) en el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="4c3a3-110">Los punteros de función se pasan a la LSA en una matriz de estructuras de [**\_ \_ tabla de la función SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .</span><span class="sxs-lookup"><span data-stu-id="4c3a3-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![LSA llama a splsamodeinitialize para obtener punteros de función](images/lsamode2.png)

<span data-ttu-id="4c3a3-112">Después de recibir el conjunto de estructuras de [**\_ \_ tabla de funciones de SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , LSA llama a la función [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de cada paquete de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="4c3a3-113">LSA usa esta llamada de función para pasar a cada paquete de seguridad una estructura de tabla de la [**\_ \_ función \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , que contiene punteros a las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="4c3a3-114">Además de almacenar los punteros a las funciones de compatibilidad de LSA, los paquetes de seguridad personalizados deben usar su implementación de la función **SpInitialize** para realizar cualquier procesamiento relacionado con la inicialización.</span><span class="sxs-lookup"><span data-stu-id="4c3a3-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="4c3a3-115">Para obtener una lista de las funciones de compatibilidad de LSA disponibles para los paquetes de seguridad de modo LSA, consulte [funciones de LSA llamadas por SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a3-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="4c3a3-116">Para obtener información acerca del registro de un archivo DLL SSP/AP, consulte [registro de dll de SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="4c3a3-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
