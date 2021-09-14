---
title: CounterItem.Width, propiedad
description: Recupera o establece el ancho de línea utilizado para representar el valor del contador.
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Propiedad Width SysMon
- Propiedad Width SysMon, clase CounterItem
- Clase CounterItem SysMon, propiedad Width
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068867"
---
# <a name="counteritemwidth-property"></a>CounterItem.Width, propiedad

Recupera o establece el ancho de línea utilizado para representar el valor del contador.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
Property Width As Long
```



## <a name="property-value"></a>Valor de propiedad

Ancho de línea usado en un gráfico de líneas. Los valores válidos oscilan entre 1 y 3, donde 1 (el valor predeterminado) es el ancho más estrecho.

**Antes de Windows Vista:** Los valores válidos oscilan entre 1 y 9. No use un valor de ancho mayor que 3 si la aplicación se ejecutará en Windows Vista.

## <a name="exceptions"></a>Excepciones



| Tipo de excepción               | Condición                              |
|------------------------------|----------------------------------------|
| **System.ArgumentException** | El ancho de línea especificado no es válido. |



 

## <a name="remarks"></a>Observaciones

El ancho de línea predeterminado para los primeros dieciséis contadores que agregue es 1. El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 17 - 32) que agregue es 2. El ancho de línea predeterminado para los siguientes dieciséis contadores (contadores 33 - 48) que agregue es 3. Después, SYSMON elige aleatoriamente el ancho de línea. Para obtener más información, [**vea CounterItem.Color**](counteritem-color.md).

Para especificar un [**estilo de línea**](counteritem-linestyle.md) distinto de sólido, el ancho debe ser 1. Si especifica un valor mayor que 1 y especifica un estilo de línea no sólido, SYSMON omite el ancho de línea especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                            |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





