---
title: Seguridad de Server-Side
description: Seguridad de Server-Side
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77501c395c3ae1f14c8451d4691e7e776545e756
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995665"
---
# <a name="server-side-security"></a>Seguridad de Server-Side

El servidor puede recuperar información de seguridad sobre un llamador o suplantar al autor de la llamada mediante los métodos de [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity). COM proporciona una implementación de **IServerSecurity** en el objeto de contexto para la llamada actual cuando se utiliza la serialización estándar. Sin embargo, es posible que esta interfaz no esté presente para algunas interfaces de serialización personalizadas.

Cuando una llamada llega al servidor, el servidor puede llamar a [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para obtener un puntero a la interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) . Con este puntero, el servidor puede llamar a los métodos **IServerSecurity** para averiguar cuál es la configuración de autenticación del cliente y suplantar al cliente, si es necesario. El objeto **IServerSecurity** es válido en cualquier subproceso del apartamento hasta que se complete la llamada representada por **IServerSecurity** . Para obtener más información sobre la suplantación, vea [suplantación](impersonation.md) y [Cloaking](cloaking.md).

También están disponibles las siguientes funciones auxiliares que se basan en la implementación de la interfaz [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) del objeto de contexto de llamada:

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 