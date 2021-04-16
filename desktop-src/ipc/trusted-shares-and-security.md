---
description: DDE de red usa recursos compartidos de confianza y descriptores de seguridad para controlar el acceso a los recursos compartidos.
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: Seguridad y recursos compartidos de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899be51745b2b27c22212c3ceeaceea016fa8d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686522"
---
# <a name="trusted-shares-and-security"></a>Seguridad y recursos compartidos de confianza

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

DDE de red usa recursos compartidos de confianza y descriptores de seguridad para controlar el acceso a los recursos compartidos.

## <a name="trusted-shares"></a>Recursos compartidos de confianza

Cuando un usuario cliente se conecta a un recurso compartido DDE desde un equipo remoto, DDE de red acepta la solicitud solo si se cumplen las siguientes instrucciones:

-   El usuario que creó el recurso compartido ha concedido el estado de confianza al recurso compartido mediante una llamada a [**NDdeSetTrustedShare**](nddesettrustedshare.md). Solo el creador del recurso compartido puede conceder el estado de confianza al recurso compartido. Ni siquiera un administrador puede conceder el estado de confianza a un recurso compartido DDE creado por otro usuario.
-   El usuario que creó el recurso compartido ha iniciado sesión actualmente en el equipo servidor.

El proceso de conceder el estado de confianza a un recurso compartido agrega el recurso compartido a la lista de recursos compartidos de confianza del usuario con sesión iniciada en el DSDM. Esto crea una relación de confianza entre el servidor y sus clientes. Una vez que un recurso compartido DDE tiene el estado de confianza, los clientes pueden conectarse a él siempre que el usuario que ha creado el recurso compartido haya iniciado sesión. Cuando el cliente se conecta al recurso compartido desde un equipo remoto, DDE de red acepta la solicitud solo si el recurso compartido aparece en la lista de recursos compartidos de confianza del usuario que ha iniciado sesión en el DSDM.

## <a name="security"></a>Seguridad

DDE de red realiza una comprobación de seguridad adicional cuando el cliente solicita datos o un vínculo. Comprueba que el servidor ha concedido al usuario remoto el permiso necesario para la operación. El servidor controla el acceso al recurso compartido a través del parámetro *pSD* de la función [**NDdeShareAdd**](nddeshareadd.md) . Este parámetro especifica el descriptor de seguridad. Si este parámetro es **null**, la función crea un descriptor de seguridad predeterminado que concede acceso completo al creador del recurso compartido y concede permiso de lectura y vinculación a todos los demás usuarios. Para conceder o denegar permisos adicionales a usuarios individuales o grupos de usuarios, cree y use un descriptor de seguridad. Para obtener más información acerca de los descriptores de seguridad, vea [**Access Control**](/windows/desktop/SecAuthZ/access-control).

Para obtener el descriptor de seguridad de un recurso compartido DDE existente, llame a la función [**NDdeGetShareSecurity**](nddegetsharesecurity.md) . Puede editar la información y, a continuación, actualizar el descriptor de seguridad para el recurso compartido mediante la función [**NDdeSetShareSecurity**](nddesetsharesecurity.md) .

 

 
