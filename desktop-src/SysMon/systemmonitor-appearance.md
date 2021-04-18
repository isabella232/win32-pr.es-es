---
title: SystemMonitor. Appearance (propiedad)
description: Recupera o establece la apariencia del control para incluir u omitir los efectos de visualización tridimensionales.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propiedad de apariencia SysMon
- Propiedad Appearance SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665925"
---
# <a name="systemmonitorappearance-property"></a>SystemMonitor. Appearance (propiedad)

Recupera o establece la apariencia del control para incluir u omitir los efectos de visualización tridimensionales.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor de apariencia que determina si el control se dibuja con efectos tridimensionales.

Puede establecer esta propiedad en uno de los siguientes valores.



| Value                                                                        | Significado                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Pinta el control sin efectos visuales.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Pinta el control con efectos tridimensionales. Este es el valor predeterminado.<br/> |



 

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                                    |
|------------------------------|----------------------------------------------|
| **System.ArgumentException** | El valor de apariencia especificado no es válido. |



 

## <a name="remarks"></a>Observaciones

Se trata de una propiedad de ambiente. El valor de esta propiedad viene determinado por el contenedor. Establecer el valor de esta propiedad puede afectar a la ilusión del control y el contenedor como una sola aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





