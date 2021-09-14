---
title: Server-Side Security
description: Server-Side Security
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063910"
---
# <a name="server-side-security"></a>Server-Side Security

El servidor puede recuperar información de seguridad sobre un llamador o suplantar al autor de la llamada mediante los métodos de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). COM proporciona **una implementación de IServerSecurity** en el objeto de contexto para la llamada actual cuando se usa la serialización estándar. Sin embargo, es posible que esta interfaz no esté presente en algunas interfaces con serialización personalizada.

Cuando llega una llamada al servidor, el servidor puede llamar a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obtener un puntero a la [**interfaz IServerSecurity.**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) Con este puntero, el servidor puede llamar a los métodos **IServerSecurity** para averiguar cuál es la configuración de autenticación del cliente y suplantar al cliente, si es necesario. El **objeto IServerSecurity** es válido en cualquier subproceso del apartamento hasta que se complete la llamada representada por **IServerSecurity.** Para obtener más información sobre la suplantación, [vea Suplantación](impersonation.md) y [Suplantación.](cloaking.md)

También están disponibles las siguientes funciones auxiliares que se basan en la implementación de la interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) del objeto de contexto de llamada:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 