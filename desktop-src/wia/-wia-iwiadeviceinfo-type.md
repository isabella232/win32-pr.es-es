---
description: Recupera el tipo de dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. Type (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720391"
---
# <a name="deviceinfotype-property"></a>DeviceInfo. Type (propiedad)

Recupera el tipo de dispositivo de hardware de adquisición de imágenes de Windows (WIA). Los valores posibles son:

-   DigitalCamera
-   Escáner
-   StreamingVideo
-   Valor predeterminado

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Valor de propiedad

Cadena que recibe el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




