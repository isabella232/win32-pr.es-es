---
description: Define algunos o todos los atributos de caracteres, glifos, anchos de avance, posiciones x e y, asignaciones de caracteres a glifos, etc., para una cadena.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171941"
---
# <a name="script_string_analysis"></a>ANÁLISIS DE \_ \_ CADENAS DE SCRIPT

Define algunos o todos los atributos de caracteres, glifos, anchos de avance, posiciones x e y, asignaciones de caracteres a glifos, etc., para una cadena.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Observaciones

Se trata de una estructura opaca asignada dinámicamente y recuperada por [**ScriptStringAnalyse.**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) También es necesario para todas las **demás funciones \* ScriptString.**

Puesto que el análisis puede ser grande, es importante que la aplicación llame a [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) en cuanto haya terminado con la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Redistribuible<br/>          | Internet Explorer 5 o posterior enWindows Me/98/95<br/>                         |
| Encabezado<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Unscribe](uniscribe.md)
</dt> <dt>

[Estructuras de unidirección](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




