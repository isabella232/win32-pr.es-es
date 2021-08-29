---
description: La interfaz IInstallationResult define las siguientes propiedades.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propiedades de IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04760f6e1f7505e883b0b4208c0b4b189afc9bd8e98afa4f2b8b429ff12a33eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611275"
---
# <a name="iinstallationresult-properties"></a>Propiedades de IInstallationResult

La [**interfaz IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) define las siguientes propiedades.



| Propiedad                                                     | Descripción                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Hresult**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Obtiene el **valor HRESULT** de la excepción, si existe, que se genera durante la instalación.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Obtiene un valor booleano que indica si debe reiniciar el equipo para completar la instalación o desinstalación de una actualización. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Obtiene un [**valor OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) que especifica el resultado de una operación en una actualización.               |



 

 

 



