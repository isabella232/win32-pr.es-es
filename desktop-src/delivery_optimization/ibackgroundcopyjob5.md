---
title: Interfaz IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Use esta interfaz para consultar o establecer varios comportamientos opcionales de un trabajo.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461975"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interfaz IBackgroundCopyJob5

Use esta interfaz para consultar o establecer varios comportamientos opcionales de un trabajo.

Para obtener esta interfaz, llame al **método IBackgroundCopyJob::QueryInterface** `__uuidof(IBackgroundCopyJob5)` usando como identificador de interfaz.

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyJob5** hereda de [**IBackgroundCopyJob.**](ibackgroundcopyjob-.md) **IBackgroundCopyJob5** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyJob5** tiene estos métodos.



| Método                                                 | Descripción                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**Getproperty**](ibackgroundcopyjob5-getproperty.md) | Método genérico para obtener las propiedades del trabajo do.<br/> |
| [**Setproperty**](ibackgroundcopyjob5-setproperty.md) | Método genérico para establecer las propiedades del trabajo do.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





