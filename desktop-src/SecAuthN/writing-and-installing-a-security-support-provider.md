---
description: El diseño de SSPI permite escribir y agregar SSP adicionales al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Escribir e instalar un proveedor de soporte técnico de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667661"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="a5f25-103">Escribir e instalar un proveedor de soporte técnico de seguridad</span><span class="sxs-lookup"><span data-stu-id="a5f25-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="a5f25-104">El diseño de SSPI permite escribir y agregar SSP adicionales al sistema.</span><span class="sxs-lookup"><span data-stu-id="a5f25-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="a5f25-105">Un [*SSP*](../secgloss/s-gly.md) específico de un modelo de seguridad se puede desarrollar con una complejidad relativa o extraordinaria, en función del nivel de integración con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a5f25-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="a5f25-106">Un SSP de cliente que permite las conexiones a un nuevo tipo de servidor se puede desarrollar muy rápidamente, mientras que un SSP completo que proporciona suplantación local requiere más esfuerzo.</span><span class="sxs-lookup"><span data-stu-id="a5f25-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="a5f25-107">Los SSP se instalan mediante la actualización de un valor de **reg \_ SZ** en el registro, que se encuentra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a5f25-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="a5f25-108">**HKEY \_ \_** \\ Control CurrentControlSet **del sistema** de equipo local \\  \\  \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    </span><span class="sxs-lookup"><span data-stu-id="a5f25-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="a5f25-109">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a5f25-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="a5f25-110">Un único archivo DLL puede contener varios SSP.</span><span class="sxs-lookup"><span data-stu-id="a5f25-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f25-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5f25-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f25-112">Restricciones en relación con el registro y la instalación de un paquete de seguridad</span><span class="sxs-lookup"><span data-stu-id="a5f25-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
