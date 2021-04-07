---
description: Permite a los usuarios realizar tareas comunes como no administradores, denominadas usuarios estándar y como administradores sin necesidad de cambiar de usuario, cerrar la sesión o usar ejecutar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Control de cuentas de usuario (autorización)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002684"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="b9edf-103">Control de cuentas de usuario (autorización)</span><span class="sxs-lookup"><span data-stu-id="b9edf-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="b9edf-104">Control de cuentas de usuario (UAC) permite a los usuarios realizar tareas comunes como no administradores, denominadas usuarios estándar y como administradores sin necesidad de cambiar de usuario, cerrar la sesión o usar **Ejecutar como**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="b9edf-105">El comportamiento de UAC para el valor "no notificar nunca" ya no deshabilita UAC.</span><span class="sxs-lookup"><span data-stu-id="b9edf-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="b9edf-106">La configuración "no notificar nunca" proporciona un token de división y siempre eleva automáticamente el privilegio requerido.</span><span class="sxs-lookup"><span data-stu-id="b9edf-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="b9edf-107">Esta sutileza puede hacer que la aplicación tenga problemas de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="b9edf-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="b9edf-108">Todavía puede deshabilitar UAC mediante el uso de directivas de grupo o la configuración manual de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="b9edf-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="b9edf-109">**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** La configuración "no notificar nunca" deshabilita UAC.</span><span class="sxs-lookup"><span data-stu-id="b9edf-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="b9edf-110">Por ejemplo, si realiza los siguientes pasos para cambiar la configuración de "no notificar nunca", obtendrá resultados diferentes cuando intente crear un archivo en una carpeta que requiera privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="b9edf-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="b9edf-111">El comportamiento de Windows 8 es denegar el acceso.</span><span class="sxs-lookup"><span data-stu-id="b9edf-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="b9edf-112">El comportamiento de Windows 7 le permite crear el archivo de File.txt.</span><span class="sxs-lookup"><span data-stu-id="b9edf-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="b9edf-113">Pulse o haga clic en **iniciar**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-113">Click or tap **Start**.</span></span> <span data-ttu-id="b9edf-114">En el cuadro de búsqueda, escriba "cambiar la configuración del control de cuentas de usuario".</span><span class="sxs-lookup"><span data-stu-id="b9edf-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="b9edf-115">Pulse o haga clic en **cambiar la configuración del control de cuentas de usuario** para abrirla.</span><span class="sxs-lookup"><span data-stu-id="b9edf-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="b9edf-116">Mueva el control deslizante a no **notificar nunca**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="b9edf-117">Pulse o haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="b9edf-118">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b9edf-118">Restart your computer.</span></span>
6.  <span data-ttu-id="b9edf-119">Pulse o haga clic en **iniciar** y, a continuación, en **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="b9edf-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="b9edf-120">En el cuadro **abrir** , escriba "Cmd.exe".</span><span class="sxs-lookup"><span data-stu-id="b9edf-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="b9edf-121">Tenga en cuenta que el título de la ventana no contiene la cadena "administrador".</span><span class="sxs-lookup"><span data-stu-id="b9edf-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="b9edf-122">Escriba "echo >% WINDIR% \\ system32 \\File.txt".</span><span class="sxs-lookup"><span data-stu-id="b9edf-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="b9edf-123">UAC se agregó en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b9edf-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="b9edf-124">Una cuenta de usuario estándar es sinónimo de una cuenta de usuario en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9edf-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="b9edf-125">Las cuentas de usuario que son miembros del grupo local Administradores ejecutarán la mayoría de las aplicaciones como un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="b9edf-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="b9edf-126">Para obtener información acerca de UAC, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9edf-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="b9edf-127">Tema</span><span class="sxs-lookup"><span data-stu-id="b9edf-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="b9edf-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9edf-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9edf-129">[Instrucciones para el control de cuentas de usuario en el desarrollo de la interfaz de usuario](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="b9edf-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="b9edf-130">Información general acerca de UAC.</span><span class="sxs-lookup"><span data-stu-id="b9edf-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="b9edf-131">Desarrollo de aplicaciones que requieren privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="b9edf-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="b9edf-132">Modelos para desarrollar aplicaciones que realizan operaciones que requieren privilegios administrativos, pero que se ejecutan como un usuario estándar.</span><span class="sxs-lookup"><span data-stu-id="b9edf-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="b9edf-133">Referencia de autorización</span><span class="sxs-lookup"><span data-stu-id="b9edf-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="b9edf-134">Información detallada sobre las funciones de autorización, las interfaces, las estructuras y otros elementos de programación.</span><span class="sxs-lookup"><span data-stu-id="b9edf-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




