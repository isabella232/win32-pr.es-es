---
title: Introducción con ASP para ADSI
description: ADSI se puede usar para obtener acceso a los datos de directorio mediante una página ASP. Puede ser una manera cómoda de ejecutar tareas de administración y consultas desde una página web o proporcionar información a los empleados de una intranet.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ADSI DE ASP
- ADSI, páginas ASP
- ADSI, páginas ASP, ejemplo de código ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772955"
---
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="75a77-107">Introducción con ASP para ADSI</span><span class="sxs-lookup"><span data-stu-id="75a77-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="75a77-108">ADSI se puede usar para obtener acceso a los datos de directorio mediante una página ASP.</span><span class="sxs-lookup"><span data-stu-id="75a77-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="75a77-109">Puede ser una manera cómoda de ejecutar tareas de administración y consultas desde una página web o proporcionar información a los empleados de una intranet.</span><span class="sxs-lookup"><span data-stu-id="75a77-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="75a77-110">Una ventaja de usar ADSI con ASP es que puede crear una experiencia de usuario más enriquecida, ya que puede usar Visual Basic para crear una aplicación ADSI y ofrecerla a un usuario a través de una página web estándar.</span><span class="sxs-lookup"><span data-stu-id="75a77-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="75a77-111">Por ejemplo, puede crear una página web que permita a los empleados escribir el apellido de un empleado y obtener un número de teléfono para ese empleado, o bien crear un formulario que permita a los empleados actualizar información personal en una base de datos de recursos humanos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="75a77-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="75a77-112">El código ASP comienza con ' <% ' y termina con '% > '.</span><span class="sxs-lookup"><span data-stu-id="75a77-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="75a77-113">Puede agregar código ADSI como VBScript o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="75a77-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="75a77-114">Para crear una página ASP, puede usar un editor de páginas web, un bloc de notas u otro editor de texto o el sistema de desarrollo .NET Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="75a77-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="75a77-115">Antes de ejecutar la página ASP, configure la aplicación o el servidor IIS según las instrucciones que se encuentran en [problemas de autenticación para ADSI con ASP](authentication-issues-for-adsi-with-asp.md).</span><span class="sxs-lookup"><span data-stu-id="75a77-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="75a77-116">Un ejemplo de ASP simple: enumeración de objetos en un contenedor</span><span class="sxs-lookup"><span data-stu-id="75a77-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="75a77-117">Con un editor de páginas web, cree una nueva página HTML que acepte el nombre distintivo de un objeto contenedor.</span><span class="sxs-lookup"><span data-stu-id="75a77-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="75a77-118">Escriba el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="75a77-118">Enter the following code example.</span></span>


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



<span data-ttu-id="75a77-119">Esta página ahora puede aceptar un nombre de contenedor que se le pasa y usar ADSI para enumerar los objetos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="75a77-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="75a77-120">Cree una nueva página ASP denominada enum. asp y escriba el siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="75a77-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="75a77-121">Guarde esta página en la raíz del servidor Web local.</span><span class="sxs-lookup"><span data-stu-id="75a77-121">Save this page at the root of the local web server.</span></span>


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




