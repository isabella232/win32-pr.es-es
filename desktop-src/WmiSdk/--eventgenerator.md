---
description: Actúa como clase primaria para las clases que controlan la generación de eventos, como los eventos de temporizador.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: __EventGenerator clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0033bef55915865ba1945c9f17705ed40cd0d3db4cd572efd13cdadf99d4bbab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732907"
---
# <a name="__eventgenerator-class"></a>\_\_Clase EventGenerator

La **\_ \_ clase del sistema EventGenerator** es una clase base abstracta que actúa como clase primaria para las clases que controlan la generación de eventos, como eventos [de temporizador.](receiving-a-timed-or-repeating-event.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase EventGenerator** no define ningún miembro.

## <a name="remarks"></a>Comentarios

La **\_ \_ clase EventGenerator** se deriva de [**\_ \_ IndicationRelated ,**](--indicationrelated.md)que no tiene propiedades.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

