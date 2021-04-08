---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador escribe mensajes de depuración comunes en el depurador mediante la función OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910981"
---
# <a name="debug"></a><span data-ttu-id="f5ec1-103">Depurar</span><span class="sxs-lookup"><span data-stu-id="f5ec1-103">Debug</span></span>

<span data-ttu-id="f5ec1-104">Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador escribe mensajes de depuración comunes en el depurador mediante la función [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="f5ec1-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="f5ec1-105">Si este valor se establece en "2", el instalador escribe todos los mensajes de depuración válidos en el depurador mediante la función [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) .</span><span class="sxs-lookup"><span data-stu-id="f5ec1-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="f5ec1-106">Esta directiva solo se utiliza con fines de depuración y es posible que no se admita en versiones futuras de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="f5ec1-107">Windows Installer solo escribe las líneas de comandos en el archivo de registro si el tercer bit (0x04) se establece en el valor de la Directiva de depuración.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="f5ec1-108">Por lo tanto, para mostrar las líneas de comandos en el registro, establezca el valor de la Directiva de depuración en 7.</span><span class="sxs-lookup"><span data-stu-id="f5ec1-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="f5ec1-109">Esto no muestra las propiedades asociadas a un [control de edición](edit-control.md) con el [atributo de control de contraseña](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="f5ec1-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="f5ec1-110">Esto hará que las propiedades establecidas en la línea de comandos sean visibles en el registro aunque la propiedad esté incluida en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="f5ec1-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="f5ec1-111">Para obtener más información, vea [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="f5ec1-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="f5ec1-112">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="f5ec1-112">Registry Key</span></span>

<span data-ttu-id="f5ec1-113">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f5ec1-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f5ec1-114">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f5ec1-114">Data Type</span></span>

<span data-ttu-id="f5ec1-115">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="f5ec1-115">**REG\_DWORD**</span></span>

 

 
