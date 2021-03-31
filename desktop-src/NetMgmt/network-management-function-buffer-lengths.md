---
title: Longitudes de búfer de funciones de administración de red
description: En este tema se describen los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de redes.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903518"
---
# <a name="network-management-function-buffer-lengths"></a>Longitudes de búfer de funciones de administración de red

En este tema se describen los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de redes.

Las aplicaciones que especifican tamaños de búfer al llamar a las funciones de enumeración de administración de redes (y a varias funciones de recuperación de datos) deben especificar los búferes lo suficientemente grandes como para contener la estructura (o estructuras) de información devuelta más las cadenas a las que apuntan sus miembros. Si no especifica un búfer suficientemente grande para recibir todas las entradas disponibles, la función devuelve los datos de \_ error \_ . Las llamadas de enumeración no devuelven entradas parciales.

Algunas funciones de administración de red toman un parámetro de longitud máxima de datos de consulta, *prefmaxlen*. Este parámetro permite a una aplicación sugerir el número de bytes que el servidor debe devolver desde una llamada de función.

Si especifica el valor \_ de longitud máxima preferida \_ en el parámetro *prefmaxlen* , las funciones de administración de red asignarán la cantidad de memoria necesaria para los datos.

Para obtener más información, consulte [búferes de funciones de administración de red](network-management-function-buffers.md).

 

 




