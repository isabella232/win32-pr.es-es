---
title: Makefiles
description: Los archivos make de cada uno de los ejemplos de código de esta serie son archivos make genéricos de Microsoft Win32 y están diseñados para crearse desde la ventana del símbolo del sistema.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Archivos make estructurados Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0761cbdfb7a04b3e13cd003115dfdd1c9ea1f140421332df0b1ecaa31b7fc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961142"
---
# <a name="makefiles"></a>Makefiles

Los archivos make de cada uno de los ejemplos de código de esta serie son archivos make genéricos de Microsoft Win32 y están diseñados para crearse desde la ventana del símbolo del sistema. Suponen que las herramientas del compilador y del vinculador de Microsoft probablemente requerirán alguna modificación para trabajar con otras herramientas. La mayoría de los modificadores de línea de comandos del compilador o del vinculador se especifican mediante macros definidas en el archivo makefile make de Win32.mak incluido con el Kit de desarrollo de software de plataforma (SDK).

El Makeall.bat y cada archivo Make de ejemplo de código respectivo admiten opciones comunes, enumeradas en la tabla siguiente, para la invocación desde la ventana del símbolo del sistema para controlar la naturaleza de la compilación.



| Invocación de Nmake        | Makeall invocation          | Efecto                       |
|-------------------------|-----------------------------|------------------------------|
| **Nmake**               | **makeall**                 | Compile con información de depuración.     |
| **nmake** **nodebug=1** | **makeall** **"nodebug=1"** | Compile sin información de depuración.  |
| **nmake** **profile=1** | **makeall** **"profile=1"** | Compile con información de generación de perfiles. |
| **nmake** **tune=1**    | **makeall** **"tune=1"**    | Con la información del ajuste del conjunto de trabajo. |
| **nmake** **unicode=1** | **makeall** **"unicode=1"** | Compile para Unicode.         |
| **nmake** **clean**     | **makeall** **clean**       | Elimine los archivos binarios temporales.   |
| **nmake** **cleanall**  | **makeall** **cleanall**    | Elimine todos los archivos generados.  |



 

Para las Makeall.bat invocaciones, debe tener las comillas como se muestra. Las **opciones nodebug**, **profile** y **tune** son mutuamente excluyentes: solo puede usar una de ellas, o ninguna, para una compilación o vínculo determinados. Para compilar los ejemplos para que se ejecuten con cadenas Unicode, use la **opción "unicode=1".** El valor predeterminado es compilar para la compatibilidad tradicional con cadenas ANSI, ya que después se puede ejecutar en cualquier sistema operativo de 32 Windows bits. Puede compilar y ejecutar libremente con o sin Unicode en Windows Server 2003 y versiones posteriores, y Windows 2000 y versiones posteriores. Tenga en cuenta que APPUTIL siempre se compila con las mismas opciones que los otros ejemplos de código que puede que esté compilando por separado. Esto es especialmente cierto para la **opción "unicode=1".**

Puede usar un entorno de desarrollo integrado (IDE) de C++ de 32 bits instalado para compilar los ejemplos mediante los archivos make genéricos proporcionados. Para ello, es necesario que, dentro del IDE, controle los archivos Make genéricos como archivos Make "externos". Los archivos Make proporcionados requieren una utilidad make compatible con Microsoft NMAKE.

La mayoría de los IDE de C++ pueden reconocer estos archivos Make como externos y, sin embargo, proporcionan muchas ventajas de edición,compilación y depuración del IDE. Por ejemplo, en Microsoft Visual Studio 97 o posterior, puede usar la opción Abrir área de trabajo del menú Archivo para generar un área de trabajo; para ello, abra una copia con el nombre adecuado (por ejemplo, Exesquel.mak) del archivo Make de Win32 de ejemplo de código.

 

 




