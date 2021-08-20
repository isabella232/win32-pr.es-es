---
title: Propiedad SystemMonitor.Appearance
description: Recupera o establece la apariencia del control para incluir u omitir efectos de visualización tridimensionales.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Propiedad Appearance SysMon
- Propiedad Appearance SysMon , Clase SystemMonitor
- Clase SystemMonitor SysMon , propiedad Appearance
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
ms.openlocfilehash: c606ed69bca635fe0f261f64ed4439305dcdfb542edd4c0095e62eaa97266147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956208"
---
# <a name="systemmonitorappearance-property"></a>Propiedad SystemMonitor.Appearance

Recupera o establece la apariencia del control para incluir u omitir efectos de visualización tridimensionales.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property Appearance As Long
```



## <a name="property-value"></a>Valor de propiedad

Valor de apariencia que determina si el control se pinta con efectos tridimensionales.

Puede establecer esta propiedad en uno de los valores siguientes.



| Valor                                                                        | Significado                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Pinta el control sin efectos visuales.<br/>                                    |
| <dl> <dt>1</dt> </dl> | Pinta el control con efectos tridimensionales. Este es el valor predeterminado.<br/> |



 

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                                    |
|------------------------------|----------------------------------------------|
| **System.ArgumentException** | El valor de apariencia especificado no es válido. |



 

## <a name="remarks"></a>Comentarios

Se trata de una propiedad ambiente. El contenedor determina el valor de esta propiedad. Establecer el valor de esta propiedad podría afectar a la sensación de que el control y el contenedor son una sola aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Systemmonitor**](systemmonitor.md)
</dt> </dl>

 

 





