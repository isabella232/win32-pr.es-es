---
description: La API de agrupación del mismo nivel combina la tecnología de la API de proveedor de espacio de nombres PNRP y la API de gráficos.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Acerca de la API de agrupación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667464"
---
# <a name="about-the-grouping-api"></a>Acerca de la API de agrupación

La API de agrupación del mismo nivel combina la tecnología de la [API de proveedor de espacio de nombres PNRP](pnrp-namespace-provider-api.md) y la [API de gráficos](graphing-api.md). La agrupación agrega los dos siguientes elementos de tecnología:

-   Capa de multiplexación que permite que varias aplicaciones utilicen un gráfico, un puerto y una base de datos de registros.
-   Seguridad que garantiza que solo los elementos del mismo nivel invitados a un grupo pueden unirse y conectarse a lo largo de la duración de un grupo.

La agrupación proporciona un enfoque accesible y sencillo a las redes del mismo nivel debido al flujo de llamadas sencillo y a la mensajería segura. Esta API emplea PNRP para la detección de grupos y un proveedor de seguridad basado en PKI estándar en lugar de requerir a un desarrollador que implemente uno. Sin embargo, si la aplicación exige una mayor flexibilidad en términos de opciones de seguridad, considere la posibilidad de usar la [API de gráficos](about-the-graphing-api.md).

En la tabla siguiente se identifican los temas de esta sección de la API de agrupación:

| Tema                                                                | Descripción                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Cómo trabajar con grupos](how-to-work-with-groups.md)               | Describe el flujo de llamadas en una aplicación de agrupación del mismo nivel desde el inicio hasta el apagado.         |
| [Cómo funciona la seguridad de grupo](how-group-security-works.md)             | Describe cómo se protege la pertenencia a grupos del mismo nivel y los intercambios de datos.                      |
| [Invitar a un elemento del mismo nivel a un grupo](inviting-a-peer-to-a-group.md)         | Describe el proceso por el que se invita a los elementos del mismo nivel y se agregan a un grupo del mismo nivel.              |
| [Cómo conectarse a un grupo del mismo nivel](how-to-connect-to-a-peer-group.md) | Describe cómo un elemento del mismo nivel se conecta e interactúa con un grupo del mismo nivel.                        |
| [Administrar registros de grupo](managing-group-records.md)                 | Describe los registros de grupo del mismo nivel y cómo administrarlos como miembro y como administrador. |



 

> [!Note]  
> Las aplicaciones que usan la API de agrupación en un entorno con un firewall requieren grupos de excepciones que cubran el puerto específico de la aplicación, así como el puerto ' 3587-TCP ' para la API de agrupación y el puerto ' 3540-UDP ' para PNRP. Estos grupos de excepciones se deben habilitar cada vez que se ejecute la aplicación.

 

 

 



