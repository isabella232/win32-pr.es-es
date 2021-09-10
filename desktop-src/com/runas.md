---
title: RunAs
description: Configura una clase para que se ejecute con una cuenta de usuario específica cuando lo active un cliente remoto sin que se escriba como una aplicación de servicio.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Com de valor del Registro RunAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369712"
---
# <a name="runas"></a>RunAs

Configura una clase para que se ejecute con una cuenta de usuario específica cuando lo active un cliente remoto sin que se escriba como una aplicación de servicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Observaciones

El valor especifica el nombre de usuario y debe tener el formato *UserName*, Domain* UserName o de la cadena ***\\**  "Interactive User". También puede especificar las cadenas "nt authority \\ localservice" (para Servicio local) y "nt authority \\ networkservice" (para Servicio de red). También puede especificar la cadena "nt authority \\ system"* cuando { AppID GUID*} hace referencia a un servidor COM que ya se ha iniciado o que tiene una entrada en la \_ tabla de clases. Sin embargo, no puede usar "nt authority \\ system" con un servidor COM que aún no se haya iniciado. La contraseña predeterminada para "nt authority \\ localservice", "nt authority \\ networkservice" y "nt authority \\ system" es "" (cadena vacía).

> [!Note]  
> A Windows Vista, ya no se necesita una contraseña vacía para configurar las opciones "nt authority \\ localservice", "nt authority \\ networkservice" y "nt authority \\ system" **RunAs.**

 

Es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad, por lo que las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID producirán un error a menos que COM haya iniciado el proceso en nombre de una solicitud de activación real.

El nombre de usuario se toma del valor **RunAs** bajo la clave **AppID de la** clase. Si el nombre de usuario es "Usuario interactivo", el servidor se ejecuta en la identidad del usuario que ha iniciado sesión actualmente y está conectado al escritorio interactivo.

De lo contrario, la contraseña se recupera de una parte del registro que solo está disponible para los administradores del equipo y para el sistema. A continuación, el nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el servidor. Cuando se inicia de esta manera, el usuario se ejecuta con su propia estación de escritorio y ventana y no comparte identificadores de ventana, el Portapapeles u otros elementos de la interfaz de usuario con el usuario interactivo u otro usuario que se ejecuta en otras cuentas de usuario.

Para establecer una contraseña para una **clase RunAs,** debe usar la herramienta administrativa DCOMCNFG instalada en el directorio del sistema.

Para **las identidades RunAs** usadas por los servidores DCOM, la cuenta de usuario especificada en el valor debe tener los derechos para iniciar sesión como un trabajo por lotes. Este derecho se puede agregar mediante la herramienta administrativa directiva de seguridad local. Vaya a **Directivas locales y** abra **Asignación de derechos de usuario.** Seleccione **Iniciar sesión como un trabajo por lotes** y agregue la cuenta de usuario.

El **valor RunAs** no se usa para los servidores configurados para ejecutarse como servicios. Los servicios COM que necesitan ejecutarse con una identidad que no sea LocalSystem deben establecer el nombre de usuario y la contraseña adecuados mediante el applet del panel de control de servicios o las funciones del controlador de servicio. (Para obtener más información sobre estas funciones, vea [Servicios](/windows/desktop/Services/services)).

> [!Note]  
> A partir de Microsoft Windows Server 2003, la clase AppID se lee explícitamente de **HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ AppID,** que, a diferencia de la mayoría de las claves del Registro, no es intercambiable con **HKEY CLASSES ROOT \_ \_ \\ AppID**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> </dl>

 

 