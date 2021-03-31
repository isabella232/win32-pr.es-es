---
description: Enumera las interfaces de las API de autenticación.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277350"
---
# <a name="authentication-interfaces"></a>Interfaces de autenticación

Las interfaces de autenticación se clasifican según el uso de la manera siguiente:

-   [Interfaces de tarjeta inteligente](#smart-card-interfaces)
-   [Interfaces de uso compartido de identidad](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfaces de tarjeta inteligente

El SDK de tarjeta inteligente proporciona las siguientes interfaces COM. Los métodos para una interfaz específica se enumeran en la tabla de contenido y en la página de referencia de esa interfaz.



| Interfaz                                    | Descripción                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Administra un objeto de flujo.                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | Abre y administra una conexión a una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly).                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Autentica una aplicación, una tarjeta inteligente o un usuario.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Construye y administra una [*unidad de datos de protocolo de aplicación*](/windows/desktop/SecGloss/a-gly) de tarjeta inteligente (APDU). |
| [**ISCardDatabase**](iscarddatabase.md)     | Realiza operaciones de base de datos del [*Administrador de recursos*](/windows/desktop/SecGloss/r-gly) de tarjeta inteligente.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Realiza servicios de archivo comunes, como buscar, seleccionar, leer, escribir, crear y eliminar archivos.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Construye un comando APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Busca una tarjeta inteligente.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Administra el sistema de tarjeta inteligente.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Proporciona métodos que se usan para admitir otras interfaces COM de tarjeta inteligente. Esta interfaz se proporciona solo para la compatibilidad con versiones anteriores y ya no debe usarse.                               |
| [**ISCardVerify**](iscardverify.md)         | Comprueba o cambia la Directiva de comprobación del titular de la tarjeta (CHV).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfaces de uso compartido de identidad

El SDK de uso compartido de identidades proporciona las siguientes interfaces COM. Los métodos para una interfaz específica se enumeran en la tabla de contenido y en la página de referencia de esa interfaz.



| Interfaz                                                          | Descripción                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Permite a un proveedor de identidades asociar identidades con cuentas de usuario locales.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Permite a un proveedor de identidades notificar a una aplicación que realiza la llamada cuando se actualiza una identidad. |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Representa un proveedor de identidad.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Proporciona métodos para enumerar y administrar identidades y proveedores de identidades.              |



 

 

 
