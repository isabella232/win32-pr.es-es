---
title: Niveles de autenticación
description: Microsoft RPC proporciona varios niveles de autenticación.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268726"
---
# <a name="authentication-levels"></a>Niveles de autenticación

Microsoft RPC proporciona varios niveles de autenticación. Según el nivel de autenticación, se puede comprobar el origen del tráfico (que la entidad de seguridad envió el tráfico) cuando se establece la conexión, cuando el cliente inicia una nueva llamada a procedimiento remoto o durante cada intercambio de paquetes entre el cliente y el servidor.

Incluso cuando se comprueba el remitente del tráfico, la seguridad sigue siendo débil, puesto que dicha comprobación no garantiza que el paquete no se haya modificado o dañado en la ruta. solo comprueba que el paquete procede de la entidad de seguridad especificada. Para mayor seguridad, las aplicaciones distribuidas pueden establecer la biblioteca en tiempo de ejecución de RPC para comprobar que no se modifica ninguno de los datos intercambiados entre el cliente y el servidor. La biblioteca RPC también puede cifrar el contenido de cada paquete antes de enviarlo. En general, las aplicaciones que desean proteger su tráfico deben usar solo los dos últimos niveles: integridad y privacidad.

Tenga en cuenta que los niveles más altos de autenticación requieren una mayor sobrecarga computacional. Usted, como desarrollador, debe decidir cuál es más importante para su aplicación (velocidad o seguridad). La mayoría de los desarrolladores encontrarán que, con algunas pruebas de rendimiento, pueden alcanzar niveles de rendimiento aceptables y mantener la seguridad adecuada.

Las partes del cliente y del servidor de la aplicación distribuida deben usar el mismo nivel de autenticación. Para obtener una lista de los niveles de autenticación RPC, vea [constantes de nivel de autenticación](authentication-level-constants.md).

 

 




