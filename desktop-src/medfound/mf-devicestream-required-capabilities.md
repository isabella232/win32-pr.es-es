---
description: Especifica una lista de cadenas Unicode que representan las funciones de dispositivo requeridas por la transformación del sensor.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: MF_DEVICESTREAM_REQUIRED_CAPABILITIES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154636"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>\_ \_ Atributo required CAPABILITIES de MF DEVICESTREAM \_

Especifica una lista de cadenas Unicode que representan las funciones de dispositivo requeridas por la transformación del sensor.

## <a name="data-type"></a>Tipo de datos

**WCHAR \** _

## <a name="remarks"></a>Observaciones

Este atributo es opcional y solo es necesario si la transformación del sensor tiene acceso a un recurso protegido. El valor debe ser una lista delimitada por punto y coma de tokens de cadena definidos en [_ *DeviceCapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
