---
description: Un servicio no debe tener acceso a la \_ raíz HKEY current \_ User o HKEY \_ classes \_ , especialmente al suplantar a un usuario. En su lugar, use la función RegOpenCurrentUser o RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Servicios y el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668457"
---
# <a name="services-and-the-registry"></a><span data-ttu-id="16dc2-104">Servicios y el registro</span><span class="sxs-lookup"><span data-stu-id="16dc2-104">Services and the Registry</span></span>

<span data-ttu-id="16dc2-105">Un servicio no debe tener acceso a la raíz **HKEY \_ Current \_ User** o **HKEY \_ classes \_**, especialmente al suplantar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="16dc2-105">A service should not access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT**, especially when impersonating a user.</span></span> <span data-ttu-id="16dc2-106">En su lugar, use la función [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) o [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .</span><span class="sxs-lookup"><span data-stu-id="16dc2-106">Instead, use the [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) or [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) function.</span></span>

<span data-ttu-id="16dc2-107">Si intenta obtener acceso a **HKEY \_ Current \_ User** o **a \_ las clases HKEY \_ raíz** desde un servicio, puede producirse un error o puede parecer que funciona, pero hay una fuga subyacente que puede conducir a problemas al cargar o descargar el perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="16dc2-107">If you attempt to access **HKEY\_CURRENT\_USER** or **HKEY\_CLASSES\_ROOT** from a service it may fail, or it may appear to work but there is an underlying leak that can lead to problems loading or unloading the user profile.</span></span>

 

 
