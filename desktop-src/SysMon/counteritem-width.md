---
title: Propiedad de contraelemento. width
description: Recupera o establece el ancho de línea que se usa para representar el valor del contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propiedad ancho (SysMon)
- Propiedad Width SysMon, clase de contraelemento
- Clase de contraelemento SysMon, propiedad width
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802491"
---
# <a name="counteritemwidth-property"></a>Propiedad de contraelemento. width

Recupera o establece el ancho de línea que se usa para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property Width As Long
```



## <a name="property-value"></a>Valor de propiedad

Ancho de línea usado en un gráfico de líneas. Los valores válidos oscilan entre 1 y 3, donde 1 (el valor predeterminado) es el ancho menor.

**Antes de Windows Vista:** Los valores válidos oscilan entre 1 y 9. No use un valor de ancho mayor que 3 si la aplicación se ejecutará en Windows Vista.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | El ancho de línea especificado no es válido. |



 

## <a name="remarks"></a>Observaciones

El ancho de línea predeterminado para los primeros dieciséis contadores que se agregan es 1. El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 17-32) que se agregan es 2. El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 33-48) que agregue es 3. Después, SYSMON selecciona aleatoriamente el ancho de línea. Para obtener más información, vea el [**elemento de peritem. color**](counteritem-color.md).

Para especificar un [**estilo de línea**](counteritem-linestyle.md) distinto de Solid, el ancho debe ser 1. Si especifica un valor mayor que 1 y especifica un estilo de línea no sólida, SYSMON omite el ancho de línea especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de**](counteritem.md)
</dt> </dl>

 

 





