---
description: Las operaciones con privilegios requieren privilegios de seguridad como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver en las constantes de API de scripting), un privilegio que debe habilitarse para una cuenta que está cargando un controlador de dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Ejecutar operaciones con privilegios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706156"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="6a4f2-103">Ejecutar operaciones con privilegios</span><span class="sxs-lookup"><span data-stu-id="6a4f2-103">Executing Privileged Operations</span></span>

<span data-ttu-id="6a4f2-104">Las operaciones con privilegios requieren privilegios de seguridad como **SeLoadDriverPrivilege** (**WbemPrivilegeLoadDriver** en las [constantes de API de scripting](scripting-api-constants.md)), un privilegio que debe habilitarse para una cuenta que está cargando un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="6a4f2-105">No puede Agregar privilegios a un administrador o usuario a través de WMI, solo puede habilitar los privilegios que la cuenta ya tiene.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="6a4f2-106">Para obtener una lista de privilegios, [**consulte \_ constantes de privilegios**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6a4f2-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="6a4f2-107">De forma predeterminada, un usuario local de un equipo puede leer datos estáticos del [*repositorio WMI*](gloss-w.md), escribir en instancias proporcionadas por los proveedores y ejecutar métodos de proveedor, a menos que el proveedor aplique requisitos de seguridad especiales por sí solos.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="6a4f2-108">Solo los administradores pueden [conectarse a un equipo remoto](connecting-to-wmi-on-a-remote-computer.md), cambiar los descriptores de seguridad o cambiar los datos estáticos del repositorio WMI, como una definición de clase WMI.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="6a4f2-109">Todos los privilegios están habilitados para una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="6a4f2-110">Para obtener más información, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6a4f2-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="6a4f2-111">Las constantes de privilegios de C++ difieren de las que se usan en los lenguajes de automatización como Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="6a4f2-112">Los scripts deben usar el valor de la constante en lugar del nombre.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="6a4f2-113">Para obtener más información, vea [ejecutar operaciones con privilegios mediante C++](executing-privileged-operations-using-c-.md) o [ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="6a4f2-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="6a4f2-114">Una causa común de los errores de acceso denegado cuando se usa WMI es la falta de un privilegio habilitado para las operaciones, como obtener todas las instancias de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6a4f2-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="6a4f2-115">Sin habilitar el privilegio **SeSecurity** , no se puede tener acceso al archivo de registro de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="6a4f2-116">En el ejemplo de código de VBScript siguiente se muestra cómo establecer el privilegio **SeSecurity** en la cadena de moniker.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="6a4f2-117">Cuando se usa en el moniker, el nombre de privilegio entre paréntesis quita el "se" inicial.</span><span class="sxs-lookup"><span data-stu-id="6a4f2-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="6a4f2-118">Para obtener más información, vea [crear una cadena de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="6a4f2-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="6a4f2-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6a4f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a4f2-120">**Constantes de privilegio**</span><span class="sxs-lookup"><span data-stu-id="6a4f2-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
