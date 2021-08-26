---
title: Acerca de .NET Framework tipos de datos
description: Acerca de .NET Framework tipos de datos
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Reproductor de Windows Media,.NET Framework
- Reproductor de Windows Media de objetos, .NET Framework
- object model,.NET Framework
- Reproductor de Windows Media Móvil, .NET Framework
- Reproductor de Windows Media ActiveX control, .NET Framework
- Reproductor de Windows Media Control de ActiveX móvil, .NET Framework
- ActiveX control, .NET Framework
- .NET Framework,tipos de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36854d971b0fc220f8f77b754b08b486ff93d339935bedcf33edca39fb701e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004525"
---
# <a name="about-net-framework-data-types"></a>Acerca de .NET Framework tipos de datos

Esta sección contiene la información que necesita para traducir la referencia del modelo de objetos orientada a scripts a tipos de datos base .NET Framework Microsoft. La referencia Reproductor de Windows Media script tiene casi toda la información necesaria para usar el control Reproductor de Windows Media en un programa basado en .NET Framework y, en la mayoría de los casos, la sintaxis será similar a la de otros lenguajes de scripting como Microsoft JScript.

La Reproductor de Windows Media referencia proporciona el tipo JScript datos y, si es necesario, la conversión de C++. Por ejemplo, un **método** podría devolver un número. JScript trata todos los números de la misma manera, pero otros lenguajes distinguen entre distintos tipos de números (entero, punto flotante, y así sucesivamente). La referencia proporciona la conversión de C++ para los tipos de datos de número porque C++ puede procesar los números de forma diferente. Por ejemplo, C++ usa el tipo de datos **int** para la aritmética de enteros y **float** para el punto flotante.

El .NET Framework utiliza un sistema ligeramente diferente de tipos de datos base. En la tabla siguiente se muestran las diferencias en los tipos de datos comunes que es probable que use. Para obtener más información sobre .NET Framework tipos de datos base y la conversión a otros sistemas de tipos de datos, vea la explicación de .NET Framework Developer's Guide of System Namespace base data types (Guía del desarrollador de .NET Framework sobre los tipos de datos base del espacio de nombres del sistema).

Esta tabla proporciona el nombre .NET Framework clase y el tipo de datos de C#. Los tipos de datos para otros idiomas se definen para cada idioma en sus respectivas referencias de idioma.



| Tipo de datos de script | Tipo de datos de C++     | .NET Framework (tipo de datos de C#) |
|------------------|-------------------|---------------------------------------|
| **Number**       | **int**           | **Int32** (**int**)                   |
| **Number**       | **long**          | **Int32** (**int**)                   |
| **Number**       | **double**        | **Double** (**double**)               |
| **Number**       | **float**         | **Single** (**float**)                |
| **String**       | **Bstr**          | **String** (**string**)               |
| **Boolean**      | **VARIANT \_ BOOL** | **Booleano** (**bool**)                |
| **Object**       | **Object**        | **Object** (**object**)               |



 

Si usa Visual Studio, puede usar la tecnología Microsoft IntelliSense para determinar qué tipo de datos se espera para una función específica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Insertar el control de Reproductor de Windows Media en una .NET Framework solución**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




