---
title: Configuración de Visual Basic 6,0 para el desarrollo ADSI
description: En este tema se describe cómo configurar Visual Basic en Visual Studio para desarrollar una aplicación ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configurar Visual Basic para ADSI de desarrollo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903025"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="c6cba-104">Configuración de Visual Basic 6,0 para el desarrollo ADSI</span><span class="sxs-lookup"><span data-stu-id="c6cba-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="c6cba-105">**Configuración del entorno de desarrollo de Microsoft Visual Studio 2010 para Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="c6cba-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="c6cba-106">Inicie Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="c6cba-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="c6cba-107">Cree un nuevo proyecto de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6cba-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="c6cba-108">Agregue una referencia a la **biblioteca de tipos Active DS**.</span><span class="sxs-lookup"><span data-stu-id="c6cba-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="c6cba-109">Si no necesita el enlace de objeto COM temprano, omita este paso.</span><span class="sxs-lookup"><span data-stu-id="c6cba-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="c6cba-110">Seleccione **proyecto \| Agregar referencia**.</span><span class="sxs-lookup"><span data-stu-id="c6cba-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="c6cba-111">Seleccione la pestaña **com** .</span><span class="sxs-lookup"><span data-stu-id="c6cba-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="c6cba-112">Seleccione **biblioteca de tipos Active DS**.</span><span class="sxs-lookup"><span data-stu-id="c6cba-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="c6cba-113">Comience la programación con ADSI.</span><span class="sxs-lookup"><span data-stu-id="c6cba-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="c6cba-114">Antes de comenzar, inicie sesión en un dominio de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6cba-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="c6cba-115">Debe tener permiso para modificar la base de datos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6cba-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="c6cba-116">De forma predeterminada, el administrador tiene este privilegio.</span><span class="sxs-lookup"><span data-stu-id="c6cba-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="c6cba-117">**Una aplicación de ejemplo Visual Basic 6,0: modificar FullName y Description para un usuario**</span><span class="sxs-lookup"><span data-stu-id="c6cba-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="c6cba-118">Siga los pasos anteriores para crear un proyecto ejecutable estándar Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6cba-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="c6cba-119">Haga doble clic en el formulario.</span><span class="sxs-lookup"><span data-stu-id="c6cba-119">Double-click the Form.</span></span> <span data-ttu-id="c6cba-120">En formulario de \_ carga, escriba lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c6cba-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="c6cba-121">Debe reemplazar la cadena "LDAP:Rio = juanpérez, CN = users, DC = Fabrikam, DC = com" por el ADsPath de un usuario existente en un contenedor de su dominio.</span><span class="sxs-lookup"><span data-stu-id="c6cba-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="c6cba-122">Cree una cuenta de usuario de prueba que se pueda modificar con este fin.</span><span class="sxs-lookup"><span data-stu-id="c6cba-122">Create a test user account that can be modified for this purpose.</span></span>
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  <span data-ttu-id="c6cba-123">Presione **<F5>** para ejecutar el programa.</span><span class="sxs-lookup"><span data-stu-id="c6cba-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="c6cba-124">Para comprobar los cambios, use la herramienta de administración de usuarios y equipos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6cba-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="c6cba-125">Para obtener más información sobre el uso de ADSI y Visual Basic, consulte [acceso a Active Directory mediante Visual Basic](accessing-active-directory-using-visual-basic.md).</span><span class="sxs-lookup"><span data-stu-id="c6cba-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




