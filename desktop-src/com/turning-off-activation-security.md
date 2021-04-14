---
title: Desactivar la seguridad de activación
description: Desactivar la seguridad de activación
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da3ebd7cc03d79fc38fbafe3bc652efc3499437
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421457"
---
# <a name="turning-off-activation-security"></a>Desactivar la seguridad de activación

Normalmente, la activación utiliza la configuración de seguridad predeterminada. Sin embargo, puede controlar la seguridad de activación especificando una estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) , que es un miembro de la estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) que se pasa a las funciones de activación. Si el cliente especifica un nivel de autenticación de la autenticación de RPC \_ C \_ \_ nivel \_ ninguno en la estructura **COAUTHINFO** , no se intenta la autenticación. De lo contrario, se intenta la activación segura y, si se produce un error de autenticación, se produce un error de activación.

Si el cliente no especifica una estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) explícita y, en su lugar, establece el puntero en **null**, com intentará autenticar al cliente. Si no puede autenticar el cliente, COM comprueba el descriptor de seguridad del permiso de inicio para ver si hay una DACL **null** o una ACL que permita el acceso a todos los usuarios. Si esta comprobación se realiza correctamente, se inicia el servidor. Por lo tanto, incluso si el cliente no especifica una estructura **COAUTHINFO**, puede que tenga lugar una activación no segura cuando el servidor la permita.

> [!Note]  
> Para permitir que los usuarios de red sin autenticar ejecuten una aplicación COM, los roles de aplicación deben incluir el usuario anónimo. A partir de Windows Server 2003, de forma predeterminada, el usuario anónimo no se incluye en el grupo todos.

 

¿Por qué un cliente podría querer desactivar la seguridad de activación explícitamente aunque se lleve a cabo una activación no segura si el servidor lo permite? Dado que la desactivación explícita de la seguridad de activación aumenta el rendimiento cuando el cliente no quiere o necesita comprobaciones de seguridad.

Se deben realizar las siguientes acciones para desactivar explícitamente la seguridad de activación:

-   El cliente debe especificar un nivel de autenticación de RPC \_ C \_ authn \_ LEVEL \_ None en la estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) que sea miembro de la estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) proporcionada a la función de activación.
-   El cliente debe especificar un nivel de suplantación de \_ \_ la suplantación de nivel de Imp de RPC C \_ \_ en la estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) que sea miembro de la estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) proporcionada a la función de activación. Si no se pasa este valor, obtendrá el servidor de \_ RPC \_ S \_ no disponible.
-   El servidor debe especificar **todos** **los permisos de inicio predeterminados**. La manera recomendada para realizar esta tarea es usar Dcomcnfg.exe como se indica a continuación:
    1.  Ejecute Dcomcnfg.exe.
    2.  En la página **aplicaciones** , seleccione la aplicación que representa el servidor. Haga clic en el botón **propiedades** (o haga doble clic en la aplicación seleccionada).
    3.  En la página de propiedades **seguridad** , haga clic en el botón **usar permisos de inicio personalizados** .
    4.  Haga clic en el botón **Editar** en el área **permisos de inicio** .
    5.  En el cuadro de diálogo **permisos de valor del registro** , haga clic en el botón **Agregar** .
    6.  Seleccione la entrada para **todos** en el cuadro de lista.
    7.  En el cuadro **de lista tipo de acceso** , elija **Permitir inicio**.
    8.  Haga clic en el botón **Aceptar** .

> [!Note]  
> En Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se utiliza en la llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desactivación de la seguridad de llamadas](turning-off-call-security.md)
</dt> </dl>

 

 