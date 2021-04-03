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
# <a name="getting-started-with-asp-for-adsi"></a>Introducción con ASP para ADSI

ADSI se puede usar para obtener acceso a los datos de directorio mediante una página ASP. Puede ser una manera cómoda de ejecutar tareas de administración y consultas desde una página web o proporcionar información a los empleados de una intranet.

Una ventaja de usar ADSI con ASP es que puede crear una experiencia de usuario más enriquecida, ya que puede usar Visual Basic para crear una aplicación ADSI y ofrecerla a un usuario a través de una página web estándar. Por ejemplo, puede crear una página web que permita a los empleados escribir el apellido de un empleado y obtener un número de teléfono para ese empleado, o bien crear un formulario que permita a los empleados actualizar información personal en una base de datos de recursos humanos de la empresa.

El código ASP comienza con ' <% ' y termina con '% > '. Puede agregar código ADSI como VBScript o Visual Basic.

Para crear una página ASP, puede usar un editor de páginas web, un bloc de notas u otro editor de texto o el sistema de desarrollo .NET Microsoft Visual Studio.

Antes de ejecutar la página ASP, configure la aplicación o el servidor IIS según las instrucciones que se encuentran en [problemas de autenticación para ADSI con ASP](authentication-issues-for-adsi-with-asp.md).

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Un ejemplo de ASP simple: enumeración de objetos en un contenedor

Con un editor de páginas web, cree una nueva página HTML que acepte el nombre distintivo de un objeto contenedor. Escriba el siguiente ejemplo de código.


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



Esta página ahora puede aceptar un nombre de contenedor que se le pasa y usar ADSI para enumerar los objetos del contenedor.

Cree una nueva página ASP denominada enum. asp y escriba el siguiente ejemplo de código. Guarde esta página en la raíz del servidor Web local.


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



 

 




