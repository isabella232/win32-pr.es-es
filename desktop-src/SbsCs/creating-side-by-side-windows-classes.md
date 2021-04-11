---
description: Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Crear clases de Windows en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910641"
---
# <a name="creating-side-by-side-windows-classes"></a>Crear clases de Windows en paralelo

Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo. Mediante el uso de clases de Windows en paralelo, la aplicación puede tener versiones diferentes de una clase activa al mismo tiempo en una ventana primaria única. Para crear una clase de Windows en paralelo, la aplicación debe activar un contexto de activación antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obtener un identificador de la nueva ventana.

Por ejemplo, los controles comunes de Windows versión 5,82 y versión 6,0 tienen un control de edición. De forma predeterminada, Windows usa el control de edición de la versión 5,82. Para obtener una ventana en paralelo que tenga el control de edición de la versión 6,0, antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costumbre, la aplicación puede hacer referencia a un ensamblado que exponga clases de ventana con nombre y, a continuación, activar el contexto de activación que hace referencia a los controles de la versión 6,0.

 

 
