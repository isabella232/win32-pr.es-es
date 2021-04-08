---
description: Esta Directiva del sistema por equipo se usa solo si el registro no se ha habilitado mediante el &\# 0034;/l&\# 0034; opción de línea de comandos o por MsiEnableLog.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Registro (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813843"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="f3b80-103">Registro (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="f3b80-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="f3b80-104">Esta [Directiva del sistema](system-policy.md) por equipo se usa solo si la opción de línea de comandos "/l" o [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)no ha habilitado el registro.</span><span class="sxs-lookup"><span data-stu-id="f3b80-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="f3b80-105">Si se establece la Directiva en este caso, el instalador crea un archivo de registro en% Temp% con el nombre aleatorio: MSI \* . Inicia.</span><span class="sxs-lookup"><span data-stu-id="f3b80-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="f3b80-106">Especifique el modo de registro estableciendo el valor de la Directiva en una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f3b80-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="f3b80-107">Utilice los mismos caracteres para especificar la Directiva de modo de registro que usa la [opción de línea de comandos](command-line-options.md)"/l".</span><span class="sxs-lookup"><span data-stu-id="f3b80-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="f3b80-108">Tenga en cuenta que no puede usar "+" y " \* " para la Directiva.</span><span class="sxs-lookup"><span data-stu-id="f3b80-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="f3b80-109">El modo de registro se puede establecer mediante la Directiva, una opción de línea de comandos o mediante programación.</span><span class="sxs-lookup"><span data-stu-id="f3b80-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="f3b80-110">Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el [registro normal](normal-logging.md) en la sección [registro de Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="f3b80-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="f3b80-111">Puede evitar que se escriba información confidencial, como contraseñas, en el archivo de registro y se haga visible.</span><span class="sxs-lookup"><span data-stu-id="f3b80-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="f3b80-112">Para obtener más información, consulte [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md) .</span><span class="sxs-lookup"><span data-stu-id="f3b80-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="f3b80-113">Clave del Registro</span><span class="sxs-lookup"><span data-stu-id="f3b80-113">Registry Key</span></span>

<span data-ttu-id="f3b80-114">Establezca el valor denominado Logging en la siguiente clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f3b80-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="f3b80-115">**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f3b80-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f3b80-116">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="f3b80-116">Data Type</span></span>

<span data-ttu-id="f3b80-117">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="f3b80-117">**REG\_SZ**</span></span>

 

 



