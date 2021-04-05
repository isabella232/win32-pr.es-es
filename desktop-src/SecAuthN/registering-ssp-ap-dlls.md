---
description: Después de desarrollar un proveedor de compatibilidad de seguridad/biblioteca de vínculos dinámicos (DLL SSP/PA) que contenga uno o varios paquetes de seguridad personalizados, debe registrarlo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registro de dll de SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813590"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="a54d2-103">Registro de dll de SSP/AP</span><span class="sxs-lookup"><span data-stu-id="a54d2-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="a54d2-104">Después de desarrollar un paquete de autenticación del [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) biblioteca de vínculos dinámicos (DLL SSP/PA) que contiene uno o varios [*paquetes de seguridad*](../secgloss/s-gly.md)personalizados, debe registrarlo.</span><span class="sxs-lookup"><span data-stu-id="a54d2-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="a54d2-105">Para ello, agregue el nombre del archivo DLL de SSP/AP personalizado a los datos del siguiente valor del registro:</span><span class="sxs-lookup"><span data-stu-id="a54d2-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="a54d2-106">**HKEY \_ \_** Paquetes de \\  \\  \\  \\  \\ **seguridad** de LSA del control System CurrentControlSet de equipo local</span><span class="sxs-lookup"><span data-stu-id="a54d2-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="a54d2-107">Los datos de este valor del registro son una lista de los nombres de los archivos dll de SSP/AP, sin la extensión ". dll".</span><span class="sxs-lookup"><span data-stu-id="a54d2-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="a54d2-108">El tipo de datos para esta lista es **reg \_ multi \_ SZ** , por lo que debe haber un carácter nulo (' \\ 0 ') entre cada nombre de dll de la lista.</span><span class="sxs-lookup"><span data-stu-id="a54d2-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="a54d2-109">Normalmente, los archivos dll de SSP/AP se almacenan en el directorio% SystemRoot%/system32</span><span class="sxs-lookup"><span data-stu-id="a54d2-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="a54d2-110">Si esta es la ruta de acceso a la DLL personalizada de SSP/AP, no incluya la ruta de acceso como parte del nombre del archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="a54d2-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="a54d2-111">Sin embargo, si el archivo DLL está en una ruta de acceso diferente, incluya la ruta de acceso completa al archivo DLL en el nombre.</span><span class="sxs-lookup"><span data-stu-id="a54d2-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="a54d2-112">Cada vez que se inicia el sistema, LSA carga los archivos dll SSP/AP en esta lista y realiza la secuencia de inicialización descrita en la [inicialización en modo LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="a54d2-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="a54d2-113">Registro de un paquete de seguridad personalizado como SSP de TLS predeterminado</span><span class="sxs-lookup"><span data-stu-id="a54d2-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="a54d2-114">Después de desarrollar un proveedor de compatibilidad de seguridad de TLS personalizado y registrarlo como se describió anteriormente, también debe registrarlo como "SSP de TLS predeterminado".</span><span class="sxs-lookup"><span data-stu-id="a54d2-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="a54d2-115">Para ello, rellene el nombre del paquete de SSP personalizado a los datos del siguiente valor del registro:</span><span class="sxs-lookup"><span data-stu-id="a54d2-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="a54d2-116">**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **control** \\ **LSA** \\ **predeterminado TLS SSP**</span><span class="sxs-lookup"><span data-stu-id="a54d2-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="a54d2-117">Los datos de este valor del registro son el nombre del paquete SSP, no el nombre del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="a54d2-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="a54d2-118">El tipo de datos para esta es **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="a54d2-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="a54d2-119">Las aplicaciones de modo de usuario que usan el "SSP TLS predeterminado" usarán el valor predeterminado registrado aquí.</span><span class="sxs-lookup"><span data-stu-id="a54d2-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="a54d2-120">Este cambio no afectará a las aplicaciones en modo kernel ni a las aplicaciones en modo de usuario que usan el "proveedor de protocolo de seguridad unificada de Microsoft" u otros nombres de SSP específicos de TLS.</span><span class="sxs-lookup"><span data-stu-id="a54d2-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="a54d2-121">Esta información del registro pertenece únicamente a la DLL de SSP/PA.</span><span class="sxs-lookup"><span data-stu-id="a54d2-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="a54d2-122">Para obtener información sobre cómo registrar proveedores de compatibilidad para seguridad (SSP), consulte [escribir e instalar un proveedor de soporte técnico de seguridad](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a54d2-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="a54d2-123">Para obtener información acerca de las diferencias entre SSP/AP y dll de SSP, consulte [SSP/APS frente a SSP](ssp-aps-versus-ssps.md).</span><span class="sxs-lookup"><span data-stu-id="a54d2-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a54d2-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a54d2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a54d2-125">Restricciones en relación con el registro y la instalación de un paquete de seguridad</span><span class="sxs-lookup"><span data-stu-id="a54d2-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
