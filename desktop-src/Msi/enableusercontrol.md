---
description: Esta Directiva del sistema por equipo se puede usar para especificar que el Windows Installer pasar todas las propiedades públicas al servidor durante una instalación administrada con privilegios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155532"
---
# <a name="enableusercontrol"></a><span data-ttu-id="3cc2c-103">EnableUserControl</span><span class="sxs-lookup"><span data-stu-id="3cc2c-103">EnableUserControl</span></span>

<span data-ttu-id="3cc2c-104">En el caso de una instalación administrada, es posible que el autor del paquete tenga que limitar las propiedades públicas que se pasan al lado servidor y que un usuario que no es administrador del sistema puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-104">In the case of a managed installation, the package author may need to limit which public properties are passed to the server side and can be changed by a user that is not a system administrator.</span></span> <span data-ttu-id="3cc2c-105">Normalmente, algunas restricciones son necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-105">Some restrictions are commonly necessary to maintain a secure environment when the installation requires the installer to use elevated privileges.</span></span>

<span data-ttu-id="3cc2c-106">Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador puede pasar todas [las propiedades públicas](public-properties.md) al servidor durante una instalación administrada con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-106">If this per-machine [system policy](system-policy.md) is set to "1", then the installer can pass all [public properties](public-properties.md) to the server side during a managed installation using elevated privileges.</span></span> <span data-ttu-id="3cc2c-107">La configuración de esta directiva tiene el mismo efecto que establecer la propiedad **EnableUserControl** .</span><span class="sxs-lookup"><span data-stu-id="3cc2c-107">Setting this policy has the same effect as setting the **EnableUserControl** property.</span></span> <span data-ttu-id="3cc2c-108">La configuración de esta directiva permite que se pasen todas las propiedades públicas al servicio y que los usuarios no administrativos puedan modificarlas.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-108">Setting this policy allows all public properties to be passed to the service and to be changeable by nonadministrative users.</span></span> <span data-ttu-id="3cc2c-109">De forma predeterminada, esta Directiva no está habilitada; solo las propiedades públicas restringidas se pasan al lado del servidor y pueden ser modificadas por un usuario no administrativo.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-109">By default, this policy is not enabled; only restricted public properties are passed to the server side and changeable by a nonadministrative user.</span></span> <span data-ttu-id="3cc2c-110">Se omiten todas las demás propiedades públicas.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-110">All other public properties are ignored.</span></span>

<span data-ttu-id="3cc2c-111">Si el sistema operativo es Windows 2000, el usuario no es un administrador del sistema y la aplicación o el producto se instala con privilegios elevados, un usuario que no es administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas restringidas.</span><span class="sxs-lookup"><span data-stu-id="3cc2c-111">If the operating system is Windows 2000, the user is not a system administrator, and the application or product is being installed with elevated privileges, then a user that is not a system administrator can only override an approved list of restricted public properties.</span></span> <span data-ttu-id="3cc2c-112">Para obtener más información, consulte [propiedades públicas restringidas](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3cc2c-112">For more information see [Restricted Public Properties](restricted-public-properties.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="3cc2c-113">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="3cc2c-113">Registry Key</span></span>

<span data-ttu-id="3cc2c-114">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="3cc2c-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="3cc2c-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3cc2c-115">Data Type</span></span>

<span data-ttu-id="3cc2c-116">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="3cc2c-116">**REG\_DWORD**</span></span>

 

 



