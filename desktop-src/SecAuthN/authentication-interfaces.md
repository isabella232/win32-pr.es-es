---
description: Enumera las interfaces de las API de autenticación.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843385004095499a59593bf548ff21998c4079e48667ea0e472e4a55d1f57ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141408"
---
# <a name="authentication-interfaces"></a>Interfaces de autenticación

Las interfaces de autenticación se clasifican según el uso como se muestra a continuación:

-   [Interfaces de tarjeta inteligente](#smart-card-interfaces)
-   [Interfaces de uso compartido de identidades](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfaces de tarjeta inteligente

El SDK de tarjeta inteligente proporciona las siguientes interfaces COM. Los métodos de una interfaz específica se muestran en la tabla de contenido y en la página de referencia de esa interfaz.



| Interfaz                                    | Descripción                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Administra un objeto de secuencia.                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | Abre y administra una conexión a una [*tarjeta inteligente.*](/windows/desktop/SecGloss/s-gly)                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Autentica una aplicación, tarjeta inteligente o usuario.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Construye y administra una unidad de datos de protocolo de aplicación (APDU) de tarjeta [*inteligente.*](/windows/desktop/SecGloss/a-gly) |
| [**ISCardDatabase**](iscarddatabase.md)     | Realiza operaciones de base de datos [*del administrador de recursos de tarjeta*](/windows/desktop/SecGloss/r-gly) inteligente.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Realiza servicios de archivos comunes, como buscar, seleccionar, leer, escribir, crear y eliminar archivos.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Construye un comando APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Busca una tarjeta inteligente.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Administra el sistema de tarjetas inteligentes.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Proporciona métodos que se usan para admitir otras interfaces COM de tarjeta inteligente. Esta interfaz solo se proporciona por compatibilidad con versiones anteriores y ya no se debe usar.                               |
| [**ISCardVerify**](iscardverify.md)         | Comprueba o cambia la directiva de verificación del titular de la tarjeta (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfaces de uso compartido de identidades

El SDK de uso compartido de identidades proporciona las siguientes interfaces COM. Los métodos de una interfaz específica se muestran en la tabla de contenido y en la página de referencia de esa interfaz.



| Interfaz                                                          | Descripción                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Permite que un proveedor de identidades asocie identidades con cuentas de usuario locales.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Permite que un proveedor de identidades notifique a una aplicación que realiza la llamada cuando se actualiza una identidad. |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Representa un proveedor de identidad.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Proporciona métodos para enumerar y administrar identidades y proveedores de identidades.              |



 

 

 
