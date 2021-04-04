---
description: Las siguientes funciones se usan con Security Center de Windows.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Funciones de Security Center de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906948"
---
# <a name="windows-security-center-functions"></a>Funciones de Security Center de Windows

Las siguientes funciones se usan con Security Center de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                           | Descripción                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WscGetSecurityProviderHealth**](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | Obtiene el estado de mantenimiento agregado de las categorías de proveedor de seguridad representadas por los valores de enumeración de [**\_ \_ proveedor de seguridad de WSC**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) especificados.<br/> |
| [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | Registra una función de devolución de llamada que se va a ejecutar cuando Windows Security Center (WSC) detecta un cambio que podría afectar al estado de uno de los proveedores de seguridad.<br/>                    |
| [**WscUnRegisterChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | Cancela un registro de devolución de llamada realizado por una llamada a la función [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) .<br/>                                               |



 

 

 




