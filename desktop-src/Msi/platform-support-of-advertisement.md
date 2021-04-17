---
description: El Windows Installer admite la publicidad de aplicaciones y características.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Compatibilidad de la plataforma con el anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105653127"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="4383b-103">Compatibilidad de la plataforma con el anuncio</span><span class="sxs-lookup"><span data-stu-id="4383b-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="4383b-104">El Windows Installer admite la publicidad de aplicaciones y características.</span><span class="sxs-lookup"><span data-stu-id="4383b-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="4383b-105">Las siguientes funcionalidades de anuncio están disponibles en Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP y Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4383b-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="4383b-106">Accesos directos y sus iconos.</span><span class="sxs-lookup"><span data-stu-id="4383b-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="4383b-107">Extensiones y sus iconos especificados en la [tabla ProgID](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="4383b-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="4383b-108">Los verbos de comando y Shell registrados bajo la clave ProgId.</span><span class="sxs-lookup"><span data-stu-id="4383b-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="4383b-109">Contextos CLSID y InProcHandler.</span><span class="sxs-lookup"><span data-stu-id="4383b-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="4383b-110">La instalación a petición a través de OLE solo está disponible mediante programación a través de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) y la **función CreateObject (Visual Basic)** o la **función GetObject (Visual Basic)**.</span><span class="sxs-lookup"><span data-stu-id="4383b-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="4383b-111">La información de AppId y typelib solo se escribe cuando se instala un componente anunciado.</span><span class="sxs-lookup"><span data-stu-id="4383b-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="4383b-112">Para admitir las extensiones de nombre de archivo, el administrador debe publicar la aplicación para que Active Directory mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="4383b-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="4383b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4383b-113">Remarks</span></span>

<span data-ttu-id="4383b-114">Es posible que la instalación del producto no requiera un reinicio, pero los accesos directos anunciados no funcionarán hasta que se reinicie la máquina.</span><span class="sxs-lookup"><span data-stu-id="4383b-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="4383b-115">Los accesos directos anunciados de las instalaciones posteriores funcionan sin reiniciar.</span><span class="sxs-lookup"><span data-stu-id="4383b-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="4383b-116">Para asegurarse de que los accesos directos anunciados funcionan correctamente, el autor del paquete debe programar un reinicio forzado al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="4383b-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="4383b-117">Para evitar reinicios innecesarios del sistema, programe un reinicio para que se ejecute solo si no hay instalada ninguna versión del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4383b-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="4383b-118">Las instrucciones condicionales pueden comprobar la propiedad [**ShellAdvtSupport**](shelladvtsupport.md) y la propiedad [**Version9X**](version9x.md) .</span><span class="sxs-lookup"><span data-stu-id="4383b-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="4383b-119">Para obtener más información sobre la programación de un reinicio forzado condicional, consulte [reinicios del sistema](system-reboots.md) y [uso de propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).</span><span class="sxs-lookup"><span data-stu-id="4383b-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
