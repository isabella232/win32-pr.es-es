---
description: Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Crear clases de Windows en paralelo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271655"
---
# <a name="creating-side-by-side-windows-classes"></a>Crear clases de Windows en paralelo

Los contextos de aplicación se pueden usar para crear clases de Windows en paralelo. Mediante el uso de clases Windows en paralelo, la aplicación puede tener diferentes versiones de una clase activas al mismo tiempo en una ventana primaria sola. Para crear una clase Windows en paralelo, la aplicación debe activar un contexto de activación antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para obtener un identificador para la nueva ventana.

Por ejemplo, Windows common controls versión 5.82 y versión 6.0 tenían un control Editar. Windows usa de forma predeterminada el control Edit de la versión 5.82. Para obtener una ventana en paralelo que tenga el control Edit de la versión 6.0, antes de llamar a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) como de costumbre, la aplicación puede hacer referencia a un ensamblado que expone clases de ventana con nombre y, a continuación, activar el contexto de activación que hace referencia a los controles de la versión 6.0.

 

 
