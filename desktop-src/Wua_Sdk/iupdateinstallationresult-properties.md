---
description: La interfaz IUpdateInstallationResult define las siguientes propiedades.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propiedades de IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275536"
---
# <a name="iupdateinstallationresult-properties"></a>Propiedades de IUpdateInstallationResult

La interfaz [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) define las siguientes propiedades.



| Propiedad                                                           | Descripción                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Obtiene el valor de excepción **HRESULT** que se genera durante la operación en una actualización.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Obtiene un valor booleano que indica si se requiere un reinicio del sistema en un equipo para completar la instalación de una actualización. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Obtiene un valor [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.          |



 

 

 



