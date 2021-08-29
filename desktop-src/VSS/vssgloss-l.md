---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Servicio de instantáneas de volumen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ef027528155e3a1d72b1a8e9190fd2e2f8ebb71046dd942df37bf0467e0a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997955"
---
# <a name="l-volume-shadow-copy-service"></a>L (Servicio de instantáneas de volumen)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) H [](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**ruta de acceso lógica**
</dt> <dd>

Mecanismo para describir los componentes de un escritor. Se usa para expresar las relaciones entre los componentes, en particular su jerarquía. Por ejemplo, si un escritor administraba varios libros electrónicos, podría asignar rutas de acceso lógicas de "libro \\ \\ electrónico1" y "libro \\ electrónico2" a los componentes del grupo de archivos que contienen \\ cada libro. Las rutas de acceso lógicas son necesarias al especificar subcomponentes.

Por convención, la barra diagonal inversa " \\ " se usa para separar los elementos de una ruta de acceso lógica. Más allá de eso, no hay ninguna restricción en los caracteres que pueden aparecer en una ruta de acceso lógica que **no** sea NULL.

Una ruta de acceso lógica puede ser **NULL.** Por convención, se dice que los **componentes con** rutas de acceso lógicas NULL se encuentran en el nivel superior de la jerarquía de rutas de acceso lógicas de un escritor.

Vea también [*el componente*](vssgloss-c.md), [*subcomponente*](vssgloss-s.md).

</dd> </dl>

 

 



