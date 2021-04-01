---
description: La interfaz IInstallationResult define las siguientes propiedades.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propiedades de IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082180"
---
# <a name="iinstallationresult-properties"></a>Propiedades de IInstallationResult

La interfaz [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) define las siguientes propiedades.



| Propiedad                                                     | Descripción                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Obtiene el **HRESULT** de la excepción, si existe, que se genera durante la instalación.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Obtiene un valor booleano que indica si se debe reiniciar el equipo para completar la instalación o desinstalación de una actualización. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Obtiene un valor [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.               |



 

 

 



