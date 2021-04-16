---
title: Instrucciones generales de programación
description: Directrices para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685742"
---
# <a name="general-programming-guidelines"></a>Instrucciones generales de programación

En las secciones siguientes se proporcionan directrices generales para desarrollar aplicaciones en un entorno de Servicios de Escritorio remoto.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[Capa de compatibilidad de aplicaciones](application-compatibility-layer.md)
</dt> <dd>

Para ejecutar aplicaciones heredadas en un entorno de Servicios de Escritorio remoto, puede usar el nivel de compatibilidad de aplicaciones de Servicios de Escritorio remoto.

</dd> <dt>

[Instrucciones para aplicaciones cliente/servidor](client-server-application-guidelines.md)
</dt> <dd>

Las aplicaciones cliente/servidor no deben suponer que una conexión de un solo equipo es equivalente a una sesión de un solo usuario.

</dd> <dt>

[Supervisión de conexiones y desconexiones de sesión](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

Para registrar una aplicación con Servicios de Escritorio remoto, almacene el nombre de la aplicación de servidor de canal virtual en el registro mediante la adición de una subclave.

</dd> <dt>

[Directrices de hardware de periféricos](peripheral-hardware-guidelines.md)
</dt> <dd>

Si su dispositivo de hardware no está diseñado para funcionar a través de una sesión remota, los proveedores deben asegurarse de que el software de controlador de dispositivo fuerce la deshabilitación de la redirección del dispositivo mediante una directiva del sistema o una directiva de grupo.

</dd> <dt>

[Vinculación en tiempo de ejecución a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

La aplicación puede usar la API de Servicios de Escritorio remoto para vincular dinámicamente al Wtsapi32.dll en tiempo de ejecución. Para ello, la aplicación debe llamar a la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para cargar Wtsapi32.dll.

</dd> </dl>

 

 