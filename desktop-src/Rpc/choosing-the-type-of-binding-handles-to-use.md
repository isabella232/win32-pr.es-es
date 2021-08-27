---
title: Elegir el tipo de identificadores de enlace que se usarán
description: Elegir el tipo de identificadores de enlace que se usarán
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd35286a5bb88be3094238e0e4c43b701826bca0a7e5ad02d35c5f87f0cbdaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022925"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Elegir el tipo de identificadores de enlace que se usarán

**Procedimiento recomendado:** Si sabe qué servidor usará la aplicación, use identificadores explícitos. Si no lo hace, use la construcción de identificadores explícitos cada vez o use identificadores genéricos con rutinas de enlace **\_ y desenlazadas.** **\_**

No use identificadores implícitos ni identificadores automáticos. Los identificadores implícitos no son seguros para subprocesos y, aunque la seguridad de subprocesos pueda parecer innecesaria, podría ser necesaria más adelante. Los controladores automáticos tienen una gran sobrecarga y requieren una gran cantidad de configuración para funcionar correctamente. Sus funcionalidades de búsqueda se han reemplazado por Active Directory servicios.

Los identificadores explícitos son muy eficaces y muchas funcionalidades atractivas solo están disponibles para identificadores explícitos. Por ejemplo, si varias llamadas RPC van a ir al mismo servidor, puede construir el identificador de enlace una vez y realizar todas las llamadas con él. Este enfoque es mucho más eficaz que cualquier otro método. Si se desconoce el servidor al que se va a llamar, construya un identificador de enlace explícito para cada llamada o use identificadores de enlace genéricos.

En Microsoft™ Windows XP, el tiempo de ejecución de RPC es bastante eficaz para volver a usar y almacenar en caché las llamadas, por lo que si la llamada *n*+1 termina en el mismo servidor que la enésima llamada, RPC vuelve a usar los recursos asignados para la enésima llamada, evitando la necesidad de almacenar en caché los identificadores de enlace para mejorar el rendimiento.

 

 




