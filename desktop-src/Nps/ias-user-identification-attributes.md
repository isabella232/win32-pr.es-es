---
title: Atributos de identificación de usuario
description: La identidad del usuario que solicita la autenticación se proporciona a los archivos dll de extensión de NPS en varios atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, identificación de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685769"
---
# <a name="user-identification-attributes"></a>Atributos de identificación de usuario

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

La identidad del usuario que solicita la autenticación se proporciona a los archivos dll de extensión de NPS en varios atributos diferentes.

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

Cada atributo proporciona la identidad del usuario en un formato diferente. En general, los desarrolladores deben usar **ratStrippedUserName**. Los usos de los atributos **ratUserName** y **ratFQUserName** son más especializados.

> [!Note]  
> El atributo User-Password, **ratUserPassword**, ya se ha descifrado cuando se envía al archivo dll de extensión y se puede usar en ese formulario.

 

## <a name="ratusername"></a>ratUserName

El atributo **ratUserName** contiene el nombre que se envió realmente "a través de la conexión". NPS no ha procesado ni validado de ningún modo el contenido de este atributo. Es posible que este atributo no esté disponible en absoluto porque es posible que el usuario se haya identificado a través de un medio como el identificador del autor de la llamada.

Cuando se usa [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), si este atributo está disponible, solo está disponible en el punto de conexión del archivo dll de extensión de autenticación. El atributo **ratUserName** no está disponible en el punto de conexión del archivo dll de extensión de autorización porque, en las dll de extensión de autorización, las funciones **RadiusExtensionProcess/ex** solo ven los atributos "salientes".

Cuando se usa [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), si este atributo está disponible, está disponible en el punto de conexión del archivo dll de extensión de autenticación y en el punto de conexión del archivo dll de la extensión de autorización.

## <a name="ratstrippedusername"></a>ratStrippedUserName

**RatStrippedUserName** es la identidad del usuario después de "eliminación de territorio". Para obtener más información sobre la eliminación de territorios, vea el tema [nombres de dominio Kerberos](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) en http: \\ \\ technet2.Microsoft.com.

Este atributo puede estar presente en el punto de conexión del archivo DLL de extensión de autenticación, en el punto de conexión del archivo DLL de extensión de autorización o en ambos. Se garantiza que este atributo tiene el formato:

*Dominio ***\\*** nombre de usuario*

Donde *dominio* es el nombre de dominio NetBIOS.

## <a name="ratfqusername"></a>ratFQUserName

El atributo **ratFQUserName** es el nombre de usuario "completo".

Este atributo puede estar presente en el punto de conexión del archivo DLL de extensión de autenticación, en el punto de conexión del archivo DLL de extensión de autorización o en ambos. Sin embargo, el formato del atributo puede diferir entre los dos puntos de complemento. En el punto de conexión del archivo DLL de extensión de autenticación, este atributo siempre tendrá el formato:

*Dominio ***\\*** nombre de usuario*

El formato del atributo **ratFQUserName** en el punto de conexión del archivo dll de extensión de autorización depende de si el usuario es un usuario Active Directory.

-   Si el usuario es un usuario local, **ratFQUserName** tiene el mismo formato que para el punto de conexión del archivo dll de extensión de autenticación:

    *Dominio ***\\*** nombre de usuario*

    .

-   Si el usuario es un usuario Active Directory, **ratFQUserName** puede contener el nombre del usuario en formato "canónico". El formato canónico es el formato utilizado por el Active Directory para identificar al usuario. Es la ruta de acceso desde la raíz del árbol de Active Directory e incluye la unidad organizativa (OU) del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de los archivos dll de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Invocar los archivos dll de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 