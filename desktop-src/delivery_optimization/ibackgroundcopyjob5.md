---
title: Interfaz IBackgroundCopyJob5 (Deliveryoptimization. h)
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
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150834"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interfaz IBackgroundCopyJob5

Use esta interfaz para consultar o establecer varios comportamientos opcionales de un trabajo.

Para obtener esta interfaz, llame al método **IBackgroundCopyJob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` como identificador de interfaz.

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyJob5** hereda de [**IBackgroundCopyJob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyJob5** tiene estos métodos.



| Método                                                 | Descripción                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Método genérico para obtener las propiedades de los trabajos.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Método genérico para establecer las propiedades de los trabajos.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





