---
title: Configuración de Visual Basic 6.0 para el desarrollo de ADSI
description: En este tema se describe cómo configurar Visual Basic en Visual Studio desarrollar una aplicación ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configuración de Visual Basic adsi development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cadc9f74410dcb654a880920a83c20e6af9db1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885193"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configuración de Visual Basic 6.0 para el desarrollo de ADSI

**Configuración del entorno de Microsoft Visual Studio desarrollo de 2010 para Visual Basic**

1.  Inicie Visual Studio 2010.
2.  Cree un nuevo Visual Basic proyecto.
3.  Agregue una referencia a la **biblioteca de tipos de Active DS**.
    > [!Note]  
    > Si no necesita el enlace de objetos COM temprano, o bien ignore este paso.

     

    1.  Seleccione **Project \| Agregar referencia.**
    2.  Seleccione la **pestaña COM.**
    3.  Seleccione Active DS Type Library (Biblioteca **de tipos de Active DS).**

4.  Comience a programar con ADSI.

Antes de comenzar, inicie sesión en un dominio Windows usuario. Debe tener permiso para modificar la base de datos Active Directory datos. De forma predeterminada, el administrador tiene este privilegio.

**Un ejemplo Visual Basic aplicación 6.0: Modificar FullName y la descripción de un usuario**

1.  Siga los pasos anteriores para crear un archivo ejecutable estándar Visual Basic proyecto.
2.  Haga doble clic en el formulario. En Carga \_ de formulario, escriba lo siguiente. Debe reemplazar la cadena "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" por la ADsPath de un usuario existente en un contenedor del dominio. Cree una cuenta de usuario de prueba que se pueda modificar para este propósito.
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

    

3.  Presione **&lt; F5 &gt;** para ejecutar el programa.
4.  Para comprobar los cambios, use la herramienta Usuarios y equipos de Active Directory administración de datos. Para obtener más información sobre el uso de ADSI Visual Basic, vea [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




