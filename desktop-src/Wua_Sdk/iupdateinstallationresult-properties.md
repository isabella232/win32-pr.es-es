---
description: La interfaz IUpdateInstallationResult define las siguientes propiedades.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propiedades IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7574d6fd84afc737d67147c8b40e1e501857f6c19d69bcce4b4b7216bb9c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994415"
---
# <a name="iupdateinstallationresult-properties"></a>Propiedades IUpdateInstallationResult

La [**interfaz IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define las siguientes propiedades.



| Propiedad                                                           | Descripción                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Obtiene el **valor de excepción HRESULT** que se genera durante la operación en una actualización.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Obtiene un valor booleano que indica si se requiere un reinicio del sistema en un equipo para completar la instalación de una actualización. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Obtiene un [**valor OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.          |



 

 

 



