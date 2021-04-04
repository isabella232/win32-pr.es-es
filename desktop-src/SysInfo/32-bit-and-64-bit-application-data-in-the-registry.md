---
description: En las ventanas de 64 bits, las partes de las entradas del registro se almacenan por separado para las aplicaciones de la aplicación de 32 bits y de 64 y se asignan a vistas del registro lógico independientes mediante el redirector del registro y la reflexión del registro, ya que la versión de 64 bits de una aplicación puede usar diferentes claves y valores del registro que la versión de 32 bits. También hay claves del registro compartidas que no se redirigen ni reflejan.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Datos de aplicación de 32 bits y de 64 bits en el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910014"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="eb9e7-104">Datos de aplicación de 32 bits y de 64 bits en el registro</span><span class="sxs-lookup"><span data-stu-id="eb9e7-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="eb9e7-105">En las ventanas de 64 bits, las partes de las entradas del registro se almacenan por separado para las aplicaciones de la aplicación de 32 bits y de 64 y se asignan a vistas del registro lógico independientes mediante el [redirector del registro](/windows/desktop/WinProg64/registry-redirector) y la [reflexión del registro](/windows/desktop/WinProg64/registry-reflection), ya que la versión de 64 bits de una aplicación puede usar diferentes claves y valores del registro que la versión de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="eb9e7-106">También hay [claves del registro compartidas](/windows/desktop/WinProg64/shared-registry-keys) que no se redirigen ni reflejan.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="eb9e7-107">El elemento primario de cada nodo del registro de 64 bits es el nodo Image-Specific o no es.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="eb9e7-108">El redirector del registro dirige de forma transparente el acceso al registro de una aplicación al subnodo no es adecuado.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="eb9e7-109">El componente WOW64 crea automáticamente los subnodos de redirección en el árbol del registro con el nombre **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="eb9e7-110">Como resultado, es esencial no nombrar cualquier clave del registro que cree **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="eb9e7-111">Las \_ marcas Key WOW64 \_ 64KEY y \_ 32KEY de clave WOW64 permiten el \_ acceso explícito a la vista del registro de 64 bits y la vista de 32 bits, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="eb9e7-112">Para obtener más información, vea [obtener acceso a una vista del registro alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="eb9e7-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="eb9e7-113">Para deshabilitar y habilitar la reflexión del registro para una clave determinada, use las funciones [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) y [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="eb9e7-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="eb9e7-114">Las aplicaciones solo deben deshabilitar la reflexión para las claves del registro que crean y no intentan deshabilitar la reflexión para las claves predefinidas como **HKEY \_ local \_ Machine** o **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="eb9e7-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="eb9e7-115">Para determinar qué claves están en la lista de reflexión, utilice la función [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="eb9e7-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb9e7-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb9e7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb9e7-117">redirector del registro</span><span class="sxs-lookup"><span data-stu-id="eb9e7-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="eb9e7-118">reflexión del registro</span><span class="sxs-lookup"><span data-stu-id="eb9e7-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
