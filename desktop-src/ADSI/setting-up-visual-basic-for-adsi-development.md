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
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>Configuración de Visual Basic 6,0 para el desarrollo ADSI

**Configuración del entorno de desarrollo de Microsoft Visual Studio 2010 para Visual Basic**

1.  Inicie Visual Studio 2010.
2.  Cree un nuevo proyecto de Visual Basic.
3.  Agregue una referencia a la **biblioteca de tipos Active DS**.
    > [!Note]  
    > Si no necesita el enlace de objeto COM temprano, omita este paso.

     

    1.  Seleccione **proyecto \| Agregar referencia**.
    2.  Seleccione la pestaña **com** .
    3.  Seleccione **biblioteca de tipos Active DS**.

4.  Comience la programación con ADSI.

Antes de comenzar, inicie sesión en un dominio de Windows. Debe tener permiso para modificar la base de datos de Active Directory. De forma predeterminada, el administrador tiene este privilegio.

**Una aplicación de ejemplo Visual Basic 6,0: modificar FullName y Description para un usuario**

1.  Siga los pasos anteriores para crear un proyecto ejecutable estándar Visual Basic.
2.  Haga doble clic en el formulario. En formulario de \_ carga, escriba lo siguiente. Debe reemplazar la cadena "LDAP:Rio = juanpérez, CN = users, DC = Fabrikam, DC = com" por el ADsPath de un usuario existente en un contenedor de su dominio. Cree una cuenta de usuario de prueba que se pueda modificar con este fin.
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
4.  Para comprobar los cambios, use la herramienta de administración de usuarios y equipos de Active Directory. Para obtener más información sobre el uso de ADSI y Visual Basic, consulte [acceso a Active Directory mediante Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




