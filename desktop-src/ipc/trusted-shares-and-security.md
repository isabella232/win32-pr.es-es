---
description: DDE de red usa recursos compartidos de confianza y descriptores de seguridad para controlar el acceso a los recursos compartidos.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Seguridad y recursos compartidos de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014685"
---
# <a name="trusted-shares-and-security"></a>Seguridad y recursos compartidos de confianza

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

DDE de red usa recursos compartidos de confianza y descriptores de seguridad para controlar el acceso a los recursos compartidos.

## <a name="trusted-shares"></a>Recursos compartidos de confianza

Cuando un usuario cliente se conecta a un recurso compartido DDE desde un equipo remoto, DDE de red acepta la solicitud solo si se cumplen las siguientes instrucciones:

-   El usuario que creó el recurso compartido ha concedido el estado de confianza al recurso compartido mediante una llamada a [**NDdeSetTrustedShare**](nddesettrustedshare.md). Solo el creador del recurso compartido puede conceder al recurso compartido el estado de confianza. Ni siquiera un administrador puede conceder el estado de confianza a un recurso compartido DDE creado por otro usuario.
-   El usuario que creó el recurso compartido ha iniciado sesión actualmente en el equipo servidor.

El proceso de concesión de estado de confianza a un recurso compartido agrega el recurso compartido a la lista de recursos compartidos de confianza del usuario que ha iniciado sesión en DSDM. Esto crea una relación de confianza entre el servidor y sus clientes. Una vez que un recurso compartido DDE tiene un estado de confianza, los clientes pueden conectarse a él siempre y cuando el usuario que creó el recurso compartido haya iniciado sesión. Cuando el cliente se conecta al recurso compartido desde un equipo remoto, DDE de red acepta la solicitud solo si el recurso compartido aparece en la lista de recursos compartidos de confianza del usuario que inició sesión en DSDM.

## <a name="security"></a>Seguridad

DDE de red realiza una comprobación de seguridad adicional cuando el cliente solicita datos o un vínculo. Comprueba que el servidor ha concedido al usuario remoto el permiso necesario para la operación. El servidor controla el acceso al recurso compartido a través del *parámetro pSD* de la [**función NDdeShareAdd.**](nddeshareadd.md) Este parámetro especifica el descriptor de seguridad. Si este parámetro es **NULL,** la función crea un descriptor de seguridad predeterminado que concede acceso completo al creador del recurso compartido y concede permiso de lectura y vínculo a todos los demás usuarios. Para conceder o denegar permisos adicionales a usuarios individuales o grupos de usuarios, cree y use un descriptor de seguridad. Para obtener más información sobre los descriptores de seguridad, [**vea Access Control**](/windows/desktop/SecAuthZ/access-control).

Para obtener el descriptor de seguridad de un recurso compartido de DDE existente, llame a la [**función NDdeGetShareSecurity.**](nddegetsharesecurity.md) Puede editar la información y, a continuación, actualizar el descriptor de seguridad para el recurso compartido mediante la [**función NDdeSetShareSecurity.**](nddesetsharesecurity.md)

 

 
