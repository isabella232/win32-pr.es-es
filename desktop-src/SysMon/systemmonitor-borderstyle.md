---
title: Propiedad SystemMonitor.BorderStyle
description: Recupera o establece el estilo de borde del control.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propiedad BorderStyle SysMon
- Propiedad BorderStyle SysMon , clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6175055be13adb4ac7e3ddca44d310f275138f1ff2f59ac1857ced9e14f1c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956154"
---
# <a name="systemmonitorborderstyle-property"></a>Propiedad SystemMonitor.BorderStyle

Recupera o establece el estilo de borde del control.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Valor de propiedad

Estilo de borde del control.

Puede establecer esta propiedad en uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                                                                                                                   | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**Sistema. Windows. Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt> </dl>                     | Sin borde. Este es el valor predeterminado.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**Sistema. Windows. Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt> </dl> | Borde fijo y único.<br/>                 |



 

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                                |
|------------------------------|------------------------------------------|
| **System.ArgumentException** | El estilo de borde especificado no es válido. |



 

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

 

 





