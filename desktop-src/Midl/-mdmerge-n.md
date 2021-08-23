---
title: Modificador /n
description: El modificador /n especifica la profundidad de composición para crear archivos de metadatos.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e9575995d80a4c61b5e91be7c5cfc1c802abed892af8cfa653f62c66e602b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430975"
---
# <a name="n-switch"></a>Modificador /n

El **modificador /n** especifica la profundidad de composición para crear archivos de metadatos.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*profundidad del \_ espacio de nombres* 
</dt> <dd>

Especifica la profundidad del espacio de nombres que se compone en un único archivo de metadatos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos son los formatos de valor posibles que puede especificar con el **modificador /n.**



| Formato del valor                   | Descripción                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Cree todos los tipos en la profundidad del espacio de nombres especificada en el modificador .               |
| -1                             | Cree todos los tipos en un archivo IDL por espacio de nombres.                              |
| <namespace>:Int32 > 0 | Cree todos los tipos con el espacio de nombres correspondiente en la profundidad especificada en el modificador. |
| <namespace>:-1           | Cree todos los tipos con el espacio de nombres correspondiente en un archivo por espacio de nombres.          |



 

En la tabla siguiente se muestran los resultados de diferentes combinaciones del modificador **/n** que trabaja en estos espacios de nombres.

-   Windows. Foundation.Collections.IIterable
-   Windows. Ui. DirectUI.Controls.Button
-   Windows. Ui. DirectUI.Controls.ListView
-   Windows. Ui. Immersive.Application.PlayTo.Target
-   Windows. Web.Syndication.RSS



| Modificadores                         | Resultado                                                                                                                                                                                                                                                       | Explicación                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | El último modificador /n invalida todos los modificadores –n anteriores.                                                                                                                                                                                                                                                                           |
| **/n:-1/n:Windows. UI:2**         | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. UI.winmd</dt> <dt>Windows. Web.Syndication.winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** siempre se compone en –n:2.</dt> <dt>**Windows. Los tipos** de interfaz de usuario se agrupan.</dt> <dt>**Windows. Web.Syndication** se compone de n:-1.</dt> </dl>       |
| **/n:1/n:Windows. Ui. DirectUI:3** | <dl> <dt>Windows. Foundation.winmd</dt> <dt>Windows. Ui. DirectUI.winmd</dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** siempre se compone en –n:2.</dt> <dt>**Windows. Ui. DirectUI** se compone en el nivel 3.</dt> <dt>Todos los demás tipos se componen en el nivel 1.</dt> </dl> |



 

Estas son las reglas para controlar varias instancias del **modificador /n.**

-   La instancia más específica se impone. Por ejemplo, si especifica **–n:A.B.C:4–n:A.B:5,** MDMERGE resuelve A.B.C.D en el nivel 4, porque A.B.C es más específico que A.B. A.B.E.F se resuelve en profundidad 5, porque coincide con A.B, pero no con A.B.C.
-   La última instancia se impone. Por ejemplo, si especifica **–n:5–n:2**, los tipos se componen en el nivel 2.
-   Se aplican ambas reglas. Si especifica –n:A.B.C:4 –n:A.B.C:1, el espacio de nombres A.B.C se compone en el nivel 1.

## <a name="examples"></a>Ejemplos

**mdmerge.exe -metadata \_ dir $(SDK \_ METADATA \_ PATH) -i $(INTERNAL \_ SDK METADATA \_ \_ PATH) -o $(OBJ \_ PATH) $O \\ \\ SystemMetadata -v -n:-1 -n:Windows. Foundation:2**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------|
| Cliente<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





