---
title: IWMDRMLicenseBackupRestoreStatus (interfaz)
description: La interfaz IWMDRMLicenseBackupRestoreStatus proporciona un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias. Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- IWMDRMLicenseBackupRestoreStatus interface windows Media Format
- IWMDRMLicenseBackupRestoreStatus interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26583a2911545cd256598025806d238c2f98f84434b4f23d9f13f952bfd15927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847044"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>IWMDRMLicenseBackupRestoreStatus (interfaz)

La **interfaz IWMDRMLicenseBackupRestoreStatus proporciona** un método para recuperar información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.

Esta interfaz se entrega con eventos de progreso generados durante las operaciones de copia de seguridad y restauración de licencias. Durante la copia de seguridad de la licencia se generan varios eventos **MEWMDRMLicenseBackupProgress,** cada uno de los cuales tiene una instancia de esta interfaz. Lo mismo sucede con los **eventos MEWMDRMLicenseRestoreProgress,** que se generan durante la restauración de la licencia.

Para recuperar un puntero a una instancia de la interfaz **IWMDRMLicenseBackupRestoreStatus,** primero debe llamar al método **IMFMediaEvent::GetValue** del evento de progreso. El valor que se recupera del evento es un puntero a la interfaz **IUnknown** del objeto que implementa la **interfaz IWMDRMLicenseBackupRestoreStatus.**

## <a name="members"></a>Miembros

La **interfaz IWMDRMLicenseBackupRestoreStatus** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMLicenseBackupRestoreStatus** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMLicenseBackupRestoreStatus** tiene estos métodos.



| Método                                                          | Descripción                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Recupera información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

