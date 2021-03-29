---
title: LocalService (Servicio local)
description: Instala un objeto como una aplicación de servicio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valor del registro LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904855"
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

Además de ejecutarse como un ejecutable del servidor local (EXE), un objeto COM también puede optar por empaquetarse para ejecutarse como una aplicación de servicio cuando se activa mediante un cliente local o remoto. Los servicios admiten numerosas características administrativas útiles e integradas en la interfaz de usuario, como iniciar, detener, pausar y reiniciar, así como la capacidad de establecer el servidor para que se ejecute en una cuenta de usuario específica y en una estación de ventana.

Un objeto escrito como un servicio se instala para que lo use COM mediante el establecimiento de un valor de **LocalService** y la realización de una instalación de servicio estándar. El valor **LocalService** debe establecerse en el nombre del servicio, tal y como se ha configurado en **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**, como valor predeterminado de **reg \_ SZ** .

Cuando se establece **LocalService** , cualquier cadena asignada a [**ServiceParameters**](serviceparameters.md) se pasa como un argumento de línea de comandos al servicio cuando se inicia.

La configuración del servicio se prefiere en muchas situaciones en las que las capacidades de las API de administración de servicios locales y remotos y la interfaz de usuario pueden ser útiles para los servicios que proporciona el objeto. Por ejemplo, el uso del marco administrativo existente de la arquitectura del servicio debe ser una opción obvia si el objeto es de larga duración o admite fácilmente conceptos como iniciar, detener, restablecer o pausar.

Los servicios se pueden configurar dinámicamente y se pueden configurar para que se ejecuten automáticamente cuando se arranque el equipo, o para que se inicien cuando una aplicación cliente los solicite.

Si va a implementar clases como servicios, debe tener en cuenta los siguientes puntos:

-   Este valor se usa en preferencia a la clave [**LocalServer32**](localserver32.md) para la activación local y remota requestsâ € "Si **LocalService** existe y hace referencia a un servicio válido, se omite la clave **LocalServer32** .
-   Actualmente, solo se puede ejecutar una instancia de una aplicación de servicio en un momento dado de un equipo. Por tanto, los servicios COM deben registrar sus objetos de clase en el inicio mediante REGCLS \_ MULTIPLEUSE para admitir varios clientes.
-   Para iniciarse e inicializarse correctamente, los servicios COM configurados para ejecutarse automáticamente cuando se inicia un equipo deben incluir RPCSS en su lista de servicios dependientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar servidores COM](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Servicios](/windows/desktop/Services/services)
</dt> </dl>

 

 