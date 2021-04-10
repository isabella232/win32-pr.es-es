---
title: Funciones de Sistema de archivos distribuido (DFS)
description: Las funciones Sistema de archivos distribuido (DFS) proporcionan la capacidad de agrupar de forma lógica los recursos compartidos en varios servidores y vincular los recursos compartidos de manera transparente a un espacio de nombres jerárquico único. DFS organiza los recursos compartidos en una red en una estructura árbol.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275064"
---
# <a name="distributed-file-system-dfs-functions"></a>Funciones de Sistema de archivos distribuido (DFS)

Las funciones Sistema de archivos distribuido (DFS) proporcionan la capacidad de agrupar de forma lógica los recursos compartidos en varios servidores y vincular los recursos compartidos de manera transparente a un espacio de nombres jerárquico único. DFS organiza los recursos compartidos en una red en una estructura árbol.

DFS admite espacios de nombres DFS *independientes* , los que tienen un servidor host y espacios *de nombres basados en dominio* que tienen varios servidores host y alta disponibilidad. Los datos de la *topología* DFS para los espacios de nombres basados en dominio se almacenan en Active Directory. Los datos incluyen la raíz DFS, los vínculos DFS y los destinos DFS.

Cada estructura de árbol DFS tiene uno o más *destinos raíz*. El destino raíz es un servidor host que ejecuta el servicio DFS. Una estructura de árbol DFS puede contener uno o más *vínculos DFS*. Cada vínculo DFS apunta a una o varias carpetas compartidas en la red. Puede Agregar, modificar y eliminar vínculos DFS desde un espacio de nombres DFS. Cuando se quita el último destino asociado a un vínculo DFS, DFS elimina el vínculo DFS en el espacio de nombres DFS. (En la documentación anterior, los vínculos DFS se denominaban puntos de unión).

Un vínculo DFS puede apuntar a una o varias carpetas compartidas; las carpetas se denominan *destinos*. Cuando los usuarios acceden a un vínculo DFS, el servidor DFS selecciona un conjunto de destinos en función de la información del sitio del cliente. El cliente tiene acceso al primer destino disponible del conjunto. Esto ayuda a distribuir las solicitudes de cliente en los posibles destinos y puede proporcionar una accesibilidad continua para los usuarios incluso cuando se produce un error en algunos servidores.

Una aplicación puede usar las funciones DFS para:

- Agregue un vínculo DFS a una raíz DFS.
- Cree o quite espacios de nombres DFS independientes y basados en dominio.
- Agregar destinos a un vínculo DFS existente.
- Quitar un vínculo DFS de una raíz DFS.
- Quitar un destino de un vínculo DFS.
- Permite ver y configurar información acerca de las raíces y los vínculos DFS.

Para obtener una lista de las funciones de DFS, consulte [funciones de sistema de archivos distribuido](distributed-file-system-functions.md).

Para obtener una lista de las estructuras DFS, vea [sistema de archivos distribuido estructuras](distributed-file-system-structures.md).

Los destinos de los equipos que ejecutan Microsoft Windows se pueden publicar en un espacio de nombres DFS. También puede publicar los recursos compartidos que no sean de Microsoft para los que los redirectores de cliente estén disponibles en un espacio de nombres DFS. Sin embargo, a diferencia de un recurso compartido que se publica en un servidor que ejecuta Windows Server, no puede hospedar una raíz DFS o proporcionar referencias a otros destinos DFS.

DFS usa el servicio de replicación de archivos de Windows Server para copiar los cambios entre destinos replicados. Los usuarios pueden modificar los archivos almacenados en un destino y el servicio de replicación de archivos propaga los cambios a los otros destinos designados. El servicio conserva el cambio más reciente en un documento o archivos.
