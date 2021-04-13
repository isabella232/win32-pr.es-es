---
title: Uso de la API de virtualización de Escritorio remoto
description: Los desarrolladores pueden usar esta API para personalizar la lógica que usa el agente de conexión a escritorio remoto para determinar el mejor destino para una conexión de cliente entrante.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, uso de la API de virtualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420832"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Uso de la API de virtualización de Escritorio remoto

El servicio de rol Terminal Services directorio de sesión (directorio de sesión de TS) permite que los servidores de Terminal Server almacenen información de usuario y de sesión en una base de datos denominada directorio de sesión. Cuando un usuario se conecta a un servidor de Terminal Server en una granja, el directorio de sesión de TS determina si el usuario ya tiene una sesión en ejecución en un servidor de Terminal Server y, en caso afirmativo, redirige al usuario a ese servidor de Terminal Server.

En Windows Server 2008, el servicio de rol directorio de sesión de TS se amplió y cambió de nombre Terminal Services agente de sesiones (agente de sesiones de TS). Además de mantener un directorio de sesiones existentes, el agente de sesiones de TS también puede Broker las conexiones entrantes. Cuando el agente de sesiones de TS recibe una conexión entrante de un usuario, comprueba su base de datos para determinar si el usuario tiene una sesión existente en un servidor de Terminal Server. Si es así, el agente de sesiones de TS redirige la conexión al mismo servidor de Terminal Server. Si no es así, el agente de sesiones de TS determina qué Terminal Server tiene el menor número de conexiones y redirige la conexión a ese servidor.

A partir de Windows Server 2008, Microsoft también lanzó una interfaz de programación de aplicaciones (API) pública para supervisar e interactuar con sesiones en servidores de Terminal Server. Esta API se describe en [conexión a escritorio remoto referencia del complemento de Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference). Con esta API, los desarrolladores pueden crear complementos de directivas personalizados que invalidan la lógica de redirección estándar del agente de sesiones de TS. Los complementos personalizados pueden redirigir las sesiones a los servidores de Terminal Server, así como a las máquinas virtuales, los escritorios virtuales, los servidores Blade y los escritorios físicos.

En Windows Server 2008 R2, la arquitectura de Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto) (anteriormente conocido como agente de sesiones de TS) se amplió para admitir conexiones a máquinas virtuales. La nueva arquitectura admite la administración de sesiones para máquinas virtuales a través de la API de virtualización de Escritorio remoto. Los desarrolladores pueden usar esta API para personalizar la lógica que usa el agente de conexión a escritorio remoto para determinar el mejor destino para una conexión de cliente entrante.

Escritorio remoto API de virtualización ofrece varias ventajas a los desarrolladores:

-   Las interfaces para trabajar con servidores de Terminal Server físicos son similares a las del trabajo con máquinas virtuales.
-   Los desarrolladores pueden reemplazar toda o parte de la lógica de redirección estándar. Los desarrolladores pueden basarse en el código que se suministra con el producto y no tienen que escribir todo desde cero.
-   No se requiere ningún agente de administración adicional en el servidor de administración o en la sesión.
-   Todavía se admiten complementos de agente de sesiones de TS desarrollados para su uso con Windows Server 2008.
-   La API también permite a los desarrolladores crear interfaces de usuario para la administración de los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) y las máquinas virtuales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de API de virtualización de Escritorio remoto](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Referencia del complemento de agente de Conexión a Escritorio remoto](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 