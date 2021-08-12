---
description: La API de agrupación del mismo nivel combina la tecnología de la API del proveedor de espacio de nombres PNRP y graphing API.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Acerca de la API de agrupación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b4cd1b2783d7605f9198e3c8171177e70b531944a8f2f707def5750dd6d985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612799"
---
# <a name="about-the-grouping-api"></a>Acerca de la API de agrupación

La API de agrupación del mismo nivel combina la tecnología de la API del proveedor de espacio [de nombres PNRP](pnrp-namespace-provider-api.md) y [graphing API.](graphing-api.md) La agrupación agrega los dos elementos de tecnología siguientes:

-   Capa de multiplexación que permite que varias aplicaciones usen un gráfico, un puerto y una base de datos de registros.
-   Seguridad que garantiza que solo los pares invitados a un grupo puedan unirse a un grupo y conectarse a lo largo de la duración de un grupo.

La agrupación proporciona un enfoque accesible y sencillo para las redes del mismo nivel debido al flujo de llamadas sencillo y a la mensajería segura. Esta API usa PNRP para la detección de grupos y un proveedor de seguridad estándar basado en PKI en lugar de requerir que un desarrollador implemente uno. Sin embargo, si la aplicación requiere una mayor flexibilidad en cuanto a las opciones de seguridad, considere la posibilidad de usar [Graphing API](about-the-graphing-api.md).

En la tabla siguiente se identifican los temas de esta sección de API de agrupación:

| Tema                                                                | Descripción                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Cómo trabajar con grupos](how-to-work-with-groups.md)               | Describe el flujo de llamadas en una aplicación de agrupación del mismo nivel desde el inicio hasta el apagado.         |
| [Funcionamiento de la seguridad de grupo](how-group-security-works.md)             | Describe cómo se protegen la pertenencia a grupos del mismo nivel y los intercambios de datos.                      |
| [Invitar a un grupo del mismo nivel](inviting-a-peer-to-a-group.md)         | Describe el proceso por el que se invita a los pares y se agregan a un grupo del mismo nivel.              |
| [Cómo Conectar a un grupo del mismo nivel](how-to-connect-to-a-peer-group.md) | Describe cómo un par se conecta a un grupo del mismo nivel e interactúa con él.                        |
| [Administración de registros de grupo](managing-group-records.md)                 | Describe los registros de grupo del mismo nivel y cómo administrarlos como miembro y como administrador. |



 

> [!Note]  
> Las aplicaciones que usan la API de agrupación en un entorno con un firewall requieren grupos de excepciones que cubren el puerto específico de la aplicación, así como el puerto "3587-TCP" para la API de agrupación y el puerto "3540-UDP" para PNRP. Estos grupos de excepciones deben habilitarse cada vez que se ejecute la aplicación.

 

 

 



