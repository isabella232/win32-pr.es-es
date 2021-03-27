---
title: " ifdef y ifndef (directivas)"
description: Directivas de preprocesador que determinan si se define una constante o una macro de preprocesador específica.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef y ifndef (directivas) HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076750"
---
# <a name="ifdef-and-ifndef-directives"></a>\#ifdef y \# ifndef (directivas)

Directivas de preprocesador que determinan si se define una constante o una macro de preprocesador específica.



| \#ifdef ( *identificador* )...  |
|---------------------------|
| \#endif                   |
| \#ifndef ( *identificador* )... |
| \#endif                   |



 

## <a name="parameters"></a>Parámetros



| Elemento                                                                              | Descripción                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificador*<br/> | Identificador de la constante o macro que se va a comprobar. <br/> |



 

## <a name="remarks"></a>Observaciones

Puede usar las \# directivas ifdef y \# ifndef en cualquier lugar donde [ \# ](dx-graphics-hlsl-appendix-pre-if.md) se pueda utilizar. La \# instrucción ifdef es equivalente a) Directive. Estas directivas solo comprueban la presencia o ausencia de identificadores definidos mediante la Directiva de [ \# definición](dx-graphics-hlsl-appendix-pre-define.md) , no para los identificadores declarados en el código fuente de C o C++.

Estas directivas se proporcionan únicamente por compatibilidad con las versiones anteriores del lenguaje. Se prefiere el uso del operador [definido](dx-graphics-hlsl-appendix-pre-if.md) con la \# Directiva if.

La \# Directiva ifndef comprueba el opuesto de la condición comprobada por \# ifdef. Si no se define el identificador, la condición es true (distinto de cero). de lo contrario, la condición es false (cero).

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



Cuando se compila con el siguiente comando, PROG. cpp se compilará en modo de prueba; de lo contrario, se compilará en el modo final.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Directivas de preprocesador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Si,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





