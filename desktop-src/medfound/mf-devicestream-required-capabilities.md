---
description: Especifica una lista de cadenas Unicode que representan las funcionalidades del dispositivo requeridas por la transformación del sensor.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: MF_DEVICESTREAM_REQUIRED_CAPABILITIES atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cb7947f97b76d558fffac23742cf3728028d47eb60133e8a805862165454e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956625"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>Atributo MF \_ DEVICESTREAM \_ REQUIRED \_ CAPABILITIES

Especifica una lista de cadenas Unicode que representan las funcionalidades del dispositivo requeridas por la transformación del sensor.

## <a name="data-type"></a>Tipo de datos

**Wchar\***

## <a name="remarks"></a>Comentarios

Este atributo es opcional y solo es necesario si la transformación del sensor accede a un recurso protegido. El valor debe ser una lista delimitada por punto y coma de tokens de cadena definidos en [**DeviceCapability.**](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
