---
title: " Directivas ifdef e ifndef"
description: Directivas de preprocesador que determinan si se define una constante o macro de preprocesador específicos.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- Directivas ifdef e ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068325"
---
# <a name="ifdef-and-ifndef-directives"></a>\#Directivas ifdef \# e ifndef

Directivas de preprocesador que determinan si se define una constante o macro de preprocesador específicos.



| \#identificador *ifdef* ...  |
|---------------------------|
| \#endif                   |
| \#Identificador *ifndef* ... |
| \#endif                   |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                              | Descripción                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/> | Identificador de la constante o macro que se comprobará. <br/> |



 

## <a name="remarks"></a>Comentarios

Puede usar las directivas ifdef e ifndef en cualquier \# lugar en el que se pueda usar \# [ \# if.](dx-graphics-hlsl-appendix-pre-if.md) La \# instrucción ifdef es equivalente a la directiva ). Estas directivas solo comprueban la presencia o ausencia de identificadores definidos mediante la directiva [ \# define,](dx-graphics-hlsl-appendix-pre-define.md) no para los identificadores declarados en el código fuente de C o C++.

Estas directivas se proporcionan únicamente por compatibilidad con las versiones anteriores del lenguaje. Se prefiere el uso [del operador](dx-graphics-hlsl-appendix-pre-if.md) definido con la \# directiva if.

La \# directiva ifndef comprueba lo contrario de la condición activada por \# ifdef. Si el identificador no está definido, la condición es true (distinto de cero); de lo contrario, la condición es false (cero).

## <a name="examples"></a>Ejemplos

El elemento identifier se puede pasar desde la línea de comandos con la opción /D. Se pueden especificar hasta 30 macros con /D. Es útil para comprobar si existe una definición, porque una definición se puede pasar desde la línea de comandos. En el ejemplo siguiente se usa este comportamiento para determinar si se debe ejecutar una aplicación en modo de prueba.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



Cuando se compila con el siguiente comando, prog.cpp se compilará en modo de prueba; De lo contrario, se compilará en modo final.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (HLSL de DirectX)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#if, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





