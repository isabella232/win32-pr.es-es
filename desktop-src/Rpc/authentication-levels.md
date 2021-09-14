---
title: Niveles de autenticación
description: RPC de Microsoft proporciona varios niveles de autenticación.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173542"
---
# <a name="authentication-levels"></a>Niveles de autenticación

RPC de Microsoft proporciona varios niveles de autenticación. Según el nivel de autenticación, el origen del tráfico (qué entidad de seguridad envió el tráfico) se puede comprobar cuando se establece la conexión, cuando el cliente inicia una nueva llamada a procedimiento remoto o durante cada intercambio de paquetes entre el cliente y el servidor.

Incluso cuando se comprueba el remitente del tráfico, la seguridad sigue siendo débil, ya que dicha comprobación no garantiza que el paquete no se haya modificado o dañado en la ruta; solo comprueba que el paquete provenía de la entidad de seguridad determinada. Para mayor seguridad, las aplicaciones distribuidas pueden establecer la biblioteca en tiempo de ejecución rpc para comprobar que no se modifica ninguno de los datos intercambiados entre el cliente y el servidor. La biblioteca RPC también puede cifrar el contenido de cada paquete antes de enviarlo. En general, las aplicaciones que desean proteger su tráfico deben usar solo los dos últimos niveles: integridad y privacidad.

Tenga en cuenta que los niveles más altos de autenticación requieren una mayor sobrecarga de cálculo. Usted, como desarrollador, debe decidir cuál es más importante para la aplicación: velocidad o seguridad. La mayoría de los desarrolladores descubren que, con algunas pruebas de rendimiento, pueden lograr niveles de rendimiento aceptables al tiempo que mantienen la seguridad adecuada.

El cliente y las partes del servidor de la aplicación distribuida deben usar el mismo nivel de autenticación. Para obtener una lista de los niveles de autenticación RPC, vea [Constantes de nivel de autenticación](authentication-level-constants.md).

 

 




