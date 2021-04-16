---
title: Propiedad SystemMonitor. GraphTitle
description: Recupera o establece el título del gráfico.
ms.assetid: 10a91b38-6963-4ef6-8b4f-9ecd1341f471
keywords:
- Propiedad GraphTitle SysMon
- Propiedad GraphTitle SysMon, clase SystemMonitor
- Clase SystemMonitor SysMon, propiedad GraphTitle
topic_type:
- apiref
api_name:
- SystemMonitor.GraphTitle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55918b67eb88b8c2c1aca99ce6e86f190ad1a395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534180"
---
# <a name="systemmonitorgraphtitle-property"></a>Propiedad SystemMonitor. GraphTitle

Recupera o establece el título del gráfico.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Property GraphTitle As String
```



## <a name="property-value"></a>Valor de propiedad

Título del gráfico. La longitud máxima del título es de 128 caracteres. Si el título supera los 128 caracteres, se trunca el título.

**Windows XP y windows 2000:** No hay ningún límite en la longitud del título.

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

 

 





