---
title: Configuración de Visual Basic 6.0 para el desarrollo adsi
description: En este tema se describe cómo configurar Visual Basic en Visual Studio desarrollar una aplicación ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- Configuración de Visual Basic adsi development ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed2e0f4cd0b56ee0167deda2e998314bb313d1a98cd0c43a9f06b495a4324f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838685"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configuración de Visual Basic 6.0 para el desarrollo adsi

**Configuración del entorno Microsoft Visual Studio desarrollo de 2010 para Visual Basic**

1.  Inicie Visual Studio 2010.
2.  Cree un nuevo Visual Basic proyecto.
3.  Agregue una referencia a la **biblioteca de tipos de Active DS.**
    > [!Note]  
    > Si no necesita el enlace de objetos COM temprano, o bien ignore este paso.

     

    1.  Seleccione **Project \| Agregar referencia.**
    2.  Seleccione la **pestaña COM.**
    3.  Seleccione Active DS Type Library (Biblioteca **de tipos de DS activa).**

4.  Comience a programar con ADSI.

Antes de comenzar, inicie sesión en un dominio Windows usuario. Debe tener permiso para modificar la base de Active Directory datos. De forma predeterminada, el administrador tiene este privilegio.

**Un ejemplo Visual Basic aplicación 6.0: modificar FullName y description para un usuario**

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

    

3.  Presione **<F5>** para ejecutar el programa.
4.  Para comprobar los cambios, use la herramienta Usuarios y equipos de Active Directory administración. Para obtener más información sobre el uso de ADSI y Visual Basic, vea [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




