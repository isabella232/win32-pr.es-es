---
title: Elección de un nivel de autenticación
description: Al elegir un nivel de autenticación, use la siguiente instrucción.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486738"
---
# <a name="choosing-an-authentication-level"></a>Elección de un nivel de autenticación

Al elegir un nivel de autenticación, use la siguiente instrucción. Si no importa si los datos que se envían se pueden interceptar y modificar, y los datos recibidos se pueden interceptar o modificar, use \_ \_ el nivel none de autenticación de RPC C \_ \_ , que es el valor predeterminado. Si los datos no se deben modificar y los datos privados no se envían ni reciben, use la integridad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ . En todos los demás casos, use la privacidad de nivel de autenticación de RPC \_ C \_ \_ \_ \_ .

No use el \_ \_ nivel predeterminado de autenticación de RPC c, conexión de nivel de autenticación de \_ \_ RPC \_ c \_ \_ , llamada de nivel de autenticación de RPC \_ \_ c \_ \_ \_ o PKT de nivel de autenticación de RPC \_ c \_ \_ \_ . Un atacante sofisticado puede romper estos niveles de autenticación y representarlos de forma ineficaz. Cada uno de estos niveles hace que sea ligeramente más difícil para un atacante interceptar y modificar los datos, y para suplantar, pero la seguridad no se logra realmente. Dado que rara vez se conoce el nivel de sofisticación de un atacante, no se recomiendan estas opciones.

 

 




