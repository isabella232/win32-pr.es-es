---
title: Elección de un nivel de autenticación
description: Al elegir un nivel de autenticación, use las siguientes instrucciones.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac5610efad7ae1149d3c6555e2a005e3870a4f0e55983a17457bfa130561f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073465"
---
# <a name="choosing-an-authentication-level"></a>Elección de un nivel de autenticación

Al elegir un nivel de autenticación, use las siguientes instrucciones. Si no importa si los datos que se envían se pueden interceptar y modificar, y los datos recibidos se pueden interceptar o modificar, use RPC \_ C \_ AUTHN LEVEL NONE, que es el valor \_ \_ predeterminado. Si no se deben modificar los datos y no se envían ni reciben datos privados, use RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY. En todos los demás casos, use RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY.

No use RPC \_ C \_ AUTHN \_ LEVEL \_ DEFAULT, RPC C \_ \_ AUTHN \_ LEVEL \_ CONNECT, RPC C \_ \_ AUTHN \_ LEVEL CALL o RPC C \_ \_ \_ AUTHN \_ LEVEL \_ PKT. Un atacante sofisticado puede interrumpir estos niveles de autenticación y hacerlos ineficaces. Cada uno de estos niveles dificulta ligeramente que un atacante intercepte y modifique los datos y suplante, pero la seguridad no se logra realmente. Puesto que el nivel de sofisticación de un atacante rara vez se conoce, no son opciones adecuadas.

 

 




