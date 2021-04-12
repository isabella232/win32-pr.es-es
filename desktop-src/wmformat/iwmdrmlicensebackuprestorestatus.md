---
title: Interfaz IWMDRMLicenseBackupRestoreStatus
description: La interfaz IWMDRMLicenseBackupRestoreStatus proporciona un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias. Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media
- Interfaz IWMDRMLicenseBackupRestoreStatus formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359260"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>Interfaz IWMDRMLicenseBackupRestoreStatus

La interfaz **IWMDRMLicenseBackupRestoreStatus** proporciona un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.

Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias. Se generan varios eventos **MEWMDRMLicenseBackupProgress** durante la copia de seguridad de la licencia, cada uno de los cuales tiene una instancia adjunta de esta interfaz. Lo mismo se aplica a los eventos **MEWMDRMLicenseRestoreProgress** , que se generan durante la restauración de la licencia.

Para recuperar un puntero a una instancia de la interfaz **IWMDRMLicenseBackupRestoreStatus** , primero debe llamar al método **IMFMediaEvent:: GetValue** del evento progress. El valor que se recupera del evento es un puntero a la interfaz **IUnknown** del objeto que implementa la interfaz **IWMDRMLicenseBackupRestoreStatus** .

## <a name="members"></a>Miembros

La interfaz **IWMDRMLicenseBackupRestoreStatus** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseBackupRestoreStatus** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMLicenseBackupRestoreStatus** tiene estos métodos.



| Método                                                          | Descripción                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Recupera información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

