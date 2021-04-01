---
title: Propiedad SystemMonitor. BorderStyle
description: Recupera o establece el estilo de borde del control.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Propiedad BorderStyle SysMon
- Propiedad BorderStyle SysMon, clase SystemMonitor
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
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905194"
---
# <a name="systemmonitorborderstyle-property"></a>Propiedad SystemMonitor. BorderStyle

Recupera o establece el estilo de borde del control.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a>Valor de propiedad

Estilo de borde del control.

Puede establecer esta propiedad en uno de los siguientes valores.



| Value                                                                                                                                                                                                                                                                                                                                                                                                   | Significado                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbBSNone**</dt> <dt>0</dt> </dl>                     | Sin borde. Este es el valor predeterminado.<br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <dt>**System. Windows. Forms. FormBorderStyle. VbFixedSingle**</dt> <dt>1</dt> </dl> | Borde fijo único.<br/>                 |



 

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                                |
|------------------------------|------------------------------------------|
| **System.ArgumentException** | El estilo de borde especificado no es válido. |



 

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

 

 





