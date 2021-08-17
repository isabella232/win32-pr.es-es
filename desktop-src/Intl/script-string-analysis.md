---
description: Define algunos o todos los atributos de caracteres, glifos, anchos de avance, posiciones x e y, asignaciones de caracteres a glifos, etc., para una cadena.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390304"
---
# <a name="script_string_analysis"></a>ANÁLISIS DE \_ \_ CADENAS DE SCRIPT

Define algunos o todos los atributos de caracteres, glifos, anchos de avance, posiciones x e y, asignaciones de caracteres a glifos, etc., para una cadena.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Comentarios

Se trata de una estructura opaca que [**scriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)asigna dinámicamente y recupera. También es necesario para todas las **demás funciones \* ScriptString.**

Dado que el análisis puede ser grande, es importante que la aplicación llame a [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) en cuanto haya terminado con la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Redistribuible<br/>          | Internet Explorer 5 o posterior enWindows Me/98/95<br/>                         |
| Header<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Estructuras de unidireccional](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




