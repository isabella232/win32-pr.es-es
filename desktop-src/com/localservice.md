---
title: LocalService (Servicio local)
description: Instala un objeto como una aplicación de servicio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valor del Registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249261"
---
# <a name="localservice"></a>LocalService (Servicio local)

Instala un objeto como una aplicación de servicio.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Observaciones

Además de ejecutarse como un ejecutable de servidor local (EXE), un objeto COM también puede optar por empaquetarse para ejecutarse como una aplicación de servicio cuando lo activa un cliente local o remoto. Los servicios admiten numerosas características administrativas útiles e integradas en la interfaz de usuario, como el inicio, la detención, la pausa y el reinicio locales y remotos, así como la capacidad de establecer el servidor para que se ejecute en una cuenta de usuario y una estación de ventana específicas.

Un objeto escrito como servicio se instala para su uso en COM estableciendo un valor **LocalService** y realizando una instalación de servicio estándar. El **valor LocalService** debe establecerse en el nombre del servicio, tal como se configura en **HKEY LOCAL MACHINE System \_ \_ \\ \\ CurrentControlSet \\ Services**, como el **valor predeterminado de REG \_ SZ.**

Cuando **se establece LocalService,** cualquier cadena asignada a [**ServiceParameters**](serviceparameters.md) se pasa como argumento de línea de comandos al servicio cuando se inicia.

La configuración del servicio se prefiere en muchas situaciones en las que las funcionalidades de las API de administración de servicios locales y remotos y la interfaz de usuario pueden ser útiles para los servicios que proporciona el objeto . Por ejemplo, aprovechar el marco administrativo existente de la arquitectura de servicio debe ser una opción obvia si el objeto es de larga duración o admite fácilmente conceptos como iniciar, detener, restablecer o pausar.

Los servicios se pueden configurar dinámicamente y se pueden configurar para que se ejecuten automáticamente cuando se inicie la máquina o que se inicien cuando lo solicite una aplicación cliente.

Si va a implementar clases como servicios, debe tener en cuenta los siguientes puntos:

-   Este valor se usa en preferencia a la clave [**LocalServer32**](localserver32.md) para las solicitudes de activación locales y remotas; si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32.**
-   Actualmente, solo una única instancia de una aplicación de servicio puede ejecutarse en un momento dado en un equipo. Por lo tanto, los servicios COM deben registrar sus objetos de clase al iniciarse mediante \_ REGCLS MULTIPLEUSE para admitir varios clientes.
-   Para iniciar e inicializar correctamente, los servicios COM configurados para ejecutarse automáticamente cuando se inicia una máquina deben incluir RPCSS en su lista de servicios dependientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de servidores COM](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Servicios](/windows/desktop/Services/services)
</dt> </dl>

 

 