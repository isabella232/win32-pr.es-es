---
title: Directrices generales de programación
description: Directrices para desarrollar aplicaciones en un Servicios de Escritorio remoto de aplicaciones.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b0e83daa98f59390408fa43f5c5f83ff547e3d0cad665d29922f4244913361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353887"
---
# <a name="general-programming-guidelines"></a>Directrices generales de programación

En las secciones siguientes se proporcionan directrices generales para desarrollar aplicaciones en un Servicios de Escritorio remoto de trabajo.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Capa de compatibilidad de aplicaciones](application-compatibility-layer.md)
</dt> <dd>

Para ejecutar aplicaciones heredadas en un entorno Servicios de Escritorio remoto, puede usar el Servicios de Escritorio remoto compatibilidad de aplicaciones.

</dd> <dt>

[Directrices de aplicación cliente/servidor](client-server-application-guidelines.md)
</dt> <dd>

Las aplicaciones cliente/servidor no deben asumir que una sola conexión de equipo es equivalente a una sesión de usuario único.

</dd> <dt>

[Supervisión de conexiones y desconexiones de sesión](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el Registro agregando una subclave.

</dd> <dt>

[Directrices de hardware periférico](peripheral-hardware-guidelines.md)
</dt> <dd>

Si su dispositivo de hardware no está diseñado para funcionar en una sesión remota, los proveedores deben asegurarse de que el software del controlador de dispositivo fuerza la deshabilitación del redireccionamiento del dispositivo mediante una directiva del sistema o una directiva de grupo.

</dd> <dt>

[Vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

La aplicación puede usar la API Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la [**función LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll.

</dd> </dl>

 

 