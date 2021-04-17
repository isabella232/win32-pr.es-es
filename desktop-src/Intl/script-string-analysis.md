---
description: Define algunos o todos los atributos de carácter, glifos, anchos de avance, posiciones x e y, asignaciones de carácter a glifo, etc., para una cadena.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653000"
---
# <a name="script_string_analysis"></a>\_análisis de cadenas de script \_

Define algunos o todos los atributos de carácter, glifos, anchos de avance, posiciones x e y, asignaciones de carácter a glifo, etc., para una cadena.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Observaciones

Se trata de una estructura opaca que se asigna dinámicamente y se recupera mediante [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). También es necesario para todas las demás funciones **ScriptString \** _.

Dado que el análisis puede ser grande, es importante que la aplicación llame a [_ *ScriptStringFree* *](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) en cuanto termine con la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Redistribuible<br/>          | Internet Explorer 5 o posterior Windows Me/98/95<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estructuras de Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




