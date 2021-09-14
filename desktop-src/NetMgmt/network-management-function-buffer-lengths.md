---
title: Longitudes del búfer de la función de administración de redes
description: En este tema se de abordan los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de red.
ms.assetid: 08599966-68a1-420b-bbc7-6daac833d08f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5003f739d235a099adb9f4f403c15c67bd9169e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245421"
---
# <a name="network-management-function-buffer-lengths"></a>Longitudes del búfer de la función de administración de redes

En este tema se de abordan los requisitos para las longitudes de búfer de función cuando se usan con las API de administración de red.

Las aplicaciones que especifican tamaños de búfer al llamar a funciones de enumeración de administración de red (y varias funciones de recuperación de datos) deben especificar búferes lo suficientemente grandes como para contener la estructura de información (o estructuras) devuelta, además de las cadenas a las que apuntan sus miembros. Si no especifica un búfer lo suficientemente grande como para recibir todas las entradas disponibles, la función devuelve ERROR \_ MORE \_ DATA. Las llamadas de enumeración no devuelven entradas parciales.

Algunas funciones de administración de red toman un parámetro de longitud de datos máximo de aviso, *prefmaxlen*. Este parámetro permite a una aplicación sugerir el número de bytes que el servidor debe devolver de una llamada de función.

Si especifica el valor MAX PREFERRED LENGTH en el \_ \_ parámetro *prefmaxlen,* las funciones de administración de red asignan la cantidad de memoria necesaria para los datos.

Para obtener más información, vea [Búferes de función de administración de redes.](network-management-function-buffers.md)

 

 




