---
description: El compilador MOF acepta un valor de punto flotante especificado para una propiedad nonfloating-point. El valor se redondea hacia arriba o hacia abajo y se almacena como un número de punto de no anfloating. Esta situación puede provocar algunos resultados inesperados.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilación de código MOF con Floating-Point valores
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569385"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Compilación de código MOF con Floating-Point valores

El compilador MOF acepta un valor de punto flotante especificado para una propiedad nonfloating-point. El valor se redondea hacia arriba o hacia abajo y se almacena como un número de punto de no anfloating. Esta situación puede provocar algunos resultados inesperados.

En el siguiente ejemplo de código MOF se define una clase denominada **abc** en un espacio de nombres denominado "Test". Este código MOF se compila sin errores, pero no se puede consultar el valor de punto flotante definido para la propiedad **exampleUint16** en la instancia que crea este código.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Si emite la consulta siguiente, se obtiene un código de error que indica una consulta no válida.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



Sin embargo, la consulta siguiente busca la instancia indicada.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar archivos MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 



