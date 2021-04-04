---
title: Acerca de los tipos de datos .NET Framework
description: Acerca de los tipos de datos .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Windows Media Player, .NET Framework
- Modelo de objetos de Windows Media Player, .NET Framework
- modelo de objetos, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Control ActiveX de Windows Media Player, .NET Framework
- Control ActiveX móvil de Windows Media Player, .NET Framework
- Control ActiveX, .NET Framework
- .NET Framework, tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076222"
---
# <a name="about-net-framework-data-types"></a>Acerca de los tipos de datos .NET Framework

Esta sección contiene la información necesaria para traducir la referencia del modelo de objetos orientado a scripts en tipos de datos base de Microsoft .NET Framework. La referencia de script de Windows Media Player tiene casi toda la información necesaria para usar el control de Windows Media Player en un programa basado en .NET Framework y, en la mayoría de los casos, la sintaxis será similar a la de otros lenguajes de scripting como Microsoft JScript.

La referencia de Media Player de Windows proporciona el tipo de datos de JScript y, si es necesario, la conversión de C++. Por ejemplo, un método puede devolver un **número** . JScript trata todos los números de la misma manera, pero otros lenguajes distinguen entre los distintos tipos de números (entero, punto flotante, etc.). La referencia proporciona la conversión de C++ para los tipos de datos numéricos, ya que los números pueden procesarse de manera diferente en C++. Por ejemplo, C++ usa el tipo de datos **int** para la aritmética de enteros y **float** para el punto flotante.

El .NET Framework utiliza un sistema ligeramente diferente de tipos de datos base. En la tabla siguiente se muestran las diferencias en los tipos de datos comunes que es probable que use. Para obtener más información sobre los tipos de datos base de .NET Framework y la conversión a otros sistemas de tipo de datos, vea la guía del desarrollador de .NET Framework sobre los tipos de datos base del espacio de nombres del sistema.

En esta tabla se proporciona el nombre de clase .NET Framework y el tipo de datos de C#. Los tipos de datos para otros idiomas se definen para cada idioma en sus referencias de idioma respectivas.



| Tipo de datos de script | Tipo de datos de C++     | Clase .NET Framework (tipo de datos de C#) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**doble**)               |
| **Number**       | **float**         | **Single** (**float**)                |
| **String**       | **UTILICEN**          | **String** (**cadena**)               |
| **Boolean**      | **VARIANTE \_ bool** | **Booleano** (**bool**)                |
| **Object**       | **Object**        | **Object** (**objeto**)               |



 

Si usa Visual Studio, puede usar la tecnología de Microsoft IntelliSense para determinar qué tipo de datos se espera para una función específica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Incrustar el control Media Player de Windows en una solución de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




