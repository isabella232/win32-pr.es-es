---
title: Atributos de identificación de usuario
description: La identidad del usuario que solicita la autenticación se proporciona a los archivos DLL de la extensión NPS en una serie de atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, identificación del usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff099b46844f2259ad127346bb1ee2bfafccf4b116f3dba86dff3e175d11c28c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128765"
---
# <a name="user-identification-attributes"></a>Atributos de identificación de usuario

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

La identidad del usuario que solicita la autenticación se proporciona a los archivos DLL de la extensión NPS en una serie de atributos diferentes.

-   **nameUserName**
-   **nameStrippedUserName**
-   **nameFQUserName**

Cada atributo proporciona la identidad del usuario en un formato diferente. En general, los desarrolladores deben **usarstrippedUserName**. Los usos de los **atributosuserName** **yquetFQUserName** son más especializados.

> [!Note]  
> El **User-Password,userUserPassword**, ya se descifra cuando se envía al archivo DLL de extensión y se puede usar en ese formato.

 

## <a name="ratusername"></a>nameUserName

El **atributouserUserName** contiene el nombre que se envió realmente "a través de la conexión". NPS no ha procesado ni validado de ninguna manera el contenido de este atributo. Es posible que este atributo no esté disponible en absoluto porque es posible que el usuario se haya identificado a través de un medio, como el identificador de autor de la llamada.

Cuando se [**usa RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), si este atributo está disponible, solo está disponible en el punto de complemento DLL de extensión de autenticación. El **atributouserUserName** no está disponible en el punto de complemento dll de la extensión de autorización porque, en los archivos DLL de la extensión de autorización, las funciones **RadiusExtensionProcess/Ex** solo ven los atributos "salientes".

Cuando se [**usa RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), si este atributo está disponible, está disponible tanto en el punto de complemento DLL de extensión de autenticación como en el punto de complemento DLL de extensión de autorización.

## <a name="ratstrippedusername"></a>nameStrippedUserName

**el atributostrippedUserName** es la identidad del usuario después de "quitar el dominio". Para obtener más información sobre la extracción de dominios, consulte el tema [Nombres de dominio](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) en http: \\ \\ technet2.microsoft.com.

Este atributo puede estar presente en el complemento DLL de extensión de autenticación, el punto de complemento DLL de extensión de autorización o ambos. Se garantiza que este atributo tiene el formato:

*Dominio* **\\** _NombreDeUsuario_

Donde *Dominio* es el nombre de dominio NetBIOS.

## <a name="ratfqusername"></a>nameFQUserName

El **atributo uuFQUserName** es el nombre de usuario "completo".

Este atributo puede estar presente en el complemento DLL de extensión de autenticación, en el punto de complemento DLL de la extensión de autorización o en ambos. Sin embargo, el formato del atributo puede diferir entre los dos puntos de complemento. En el complemento DLL de extensión de autenticación, este atributo siempre tendrá el formato siguiente:

*Dominio* **\\** _NombreDeUsuario_

El formato del **atributoélFQUserName** en el punto de complemento DLL de la extensión de autorización depende de si el usuario es Active Directory usuario.

-   Si el usuario es un usuario **localnombreDeUsuarioFQ tiene** el mismo formato que para el punto de complemento DLL de extensión de autenticación:

    *Dominio* **\\** _NombreDeUsuario_

    .

-   Si el usuario es Active Directory usuario, **el nombre** del usuario puede contener el nombre del usuario en formato "canónico". El formato canónico es el formato utilizado por el Active Directory para identificar al usuario. Es la ruta de acceso de la raíz del árbol de Active Directory e incluye la unidad organizativa (OU) del usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de los archivos DLL de extensión](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Invocación de los archivos DLL de extensión](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 