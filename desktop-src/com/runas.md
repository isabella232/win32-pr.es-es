---
title: RunAs
description: Configura una clase para que se ejecute en una cuenta de usuario específica cuando está activada por un cliente remoto sin escribirse como una aplicación de servicio.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valor del registro runas COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705033"
---
# <a name="runas"></a>RunAs

Configura una clase para que se ejecute en una cuenta de usuario específica cuando está activada por un cliente remoto sin escribirse como una aplicación de servicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Observaciones

El valor especifica el nombre de usuario y debe tener el formato *nombreDeUsuario*, *dominio ***\\*** nombreDeUsuario* o la cadena "usuario interactivo". También puede especificar las cadenas "NT Authority \\ LocalService" (para el servicio local) y "NT Authority \\ NetworkService" (para el servicio de red). También puede especificar la cadena "NT Authority \\ System" cuando {*AppID \_ GUID*} hace referencia a un servidor com que ya se ha iniciado o que tiene una entrada en la tabla de clases. Sin embargo, no puede usar "NT Authority \\ System" con un servidor com que no se haya iniciado todavía. La contraseña predeterminada para ' NT Authority \\ LocalService ', ' NT Authority \\ NetworkService ' y ' NT Authority \\ System ' es ' ' (cadena vacía).

> [!Note]  
> A partir de Windows Vista, ya no se necesita una contraseña vacía para configurar las opciones de ejecución de "NT Authority \\ LocalService", "NT Authority \\ NetworkService" y "NT Authority \\ System". 

 

Es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad, por lo que se producirá un error en las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID a menos que com haya iniciado el proceso en nombre de una solicitud de activación real.

El nombre de usuario se toma del valor **runas** de la clave **AppID** de la clase. Si el nombre de usuario es "usuario interactivo", el servidor se ejecuta en la identidad del usuario que ha iniciado sesión actualmente y está conectado al escritorio interactivo.

De lo contrario, la contraseña se recupera de una parte del registro que solo está disponible para los administradores del equipo y del sistema. El nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el servidor. Cuando se inicia de esta manera, el usuario se ejecuta con su propio escritorio y estación de ventana, y no comparte los identificadores de ventana, el portapapeles u otros elementos de la interfaz de usuario con el usuario interactivo u otro usuario que se ejecute en otras cuentas de usuario.

Para establecer una contraseña para una clase **runas** , debe usar la herramienta administrativa DCOMCNFG instalada en el directorio del sistema.

Para las identidades de **runas** utilizadas por los servidores DCOM, la cuenta de usuario especificada en el valor debe tener derechos para iniciar sesión como un trabajo por lotes. Este derecho se puede agregar mediante la herramienta administrativa de la Directiva de seguridad local. Vaya a **Directivas locales** y Abra **asignación de derechos de usuario**. Seleccione **iniciar sesión como trabajo por lotes** y agregue la cuenta de usuario.

El valor **runas** no se utiliza para los servidores configurados para ejecutarse como servicios. Los servicios COM que deben ejecutarse con una identidad distinta de LocalSystem deben establecer el nombre de usuario y la contraseña adecuados mediante el applet del panel de control de servicios o las funciones del controlador de servicio. (Para obtener más información acerca de estas funciones, consulte [servicios](/windows/desktop/Services/services)).

> [!Note]  
> A partir de Microsoft Windows Server 2003, la clase AppID se lee explícitamente desde **\_ \_ las clases de software de máquina local HKEY \\ \\ \\ AppID**, que, a diferencia de la mayoría de las claves del registro, no es intercambiable con **HKEY \_ classes \_ raíz \\ AppID**.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> </dl>

 

 