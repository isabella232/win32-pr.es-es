---
title: Archivos make
description: Los archivos make de cada uno de los ejemplos de código de esta serie son archivos make genéricos de Microsoft Win32 y están diseñados para compilarse desde la ventana del símbolo del sistema.
ms.assetid: f9944069-b536-4ae2-8411-f02c3a78978c
keywords:
- Archivos make Structured Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a15fef5818c28986232e8c2a648f43bdc096832f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357787"
---
# <a name="makefiles"></a>Archivos make

Los archivos make de cada uno de los ejemplos de código de esta serie son archivos make genéricos de Microsoft Win32 y están diseñados para compilarse desde la ventana del símbolo del sistema. Suponen que las herramientas del compilador y del enlazador de Microsoft y probablemente requerirán alguna modificación para trabajar con otras herramientas. La mayoría de los modificadores de línea de comandos del compilador/vinculador se especifican mediante macros definidas en el archivo de inclusión de archivos make de Win32. Mak incluido con el kit de desarrollo de software (SDK) de la plataforma.

El archivo Makeall.bat, y cada archivo make de ejemplo de código respectivo, admiten opciones comunes, que se enumeran en la tabla siguiente, para la invocación desde la ventana del símbolo del sistema para controlar la naturaleza de la compilación.



| Invocación de NMAKE        | Invocación de Makeall          | Efecto                       |
|-------------------------|-----------------------------|------------------------------|
| **NMAKE**               | **makeall**                 | Compilar con información de depuración.     |
| **NMake** **nodebug = 1** | **makeall** **"nodebug = 1"** | Compilar sin información de depuración.  |
| Perfil de **NMake** **= 1** | **makeall** **"Profile = 1"** | Compilar con información de generación de perfiles. |
| **NMake** **Tune = 1**    | **makeall** **"Tune = 1"**    | Con información del sintonizador del conjunto de trabajo. |
| **NMake** **Unicode = 1** | **makeall** **"Unicode = 1"** | Compilar para Unicode.         |
| **NMake** **limpio**     | **makeall** **Clean**       | Elimine los archivos binarios temporales.   |
|  **cleanAll** de NMAKE  | **makeall** **cleanAll**    | Elimine todos los archivos generados.  |



 

En el caso de las invocaciones de Makeall.bat, debe incluir las comillas como se muestra. Las opciones **nodebug**, **Profile** y **Tune** se excluyen mutuamente: solo puede usar una de ellas, o ninguna, para una compilación o un vínculo determinados. Para compilar los ejemplos para que se ejecuten con cadenas Unicode, use la opción **"Unicode = 1"** . El valor predeterminado es compilar para la compatibilidad con cadenas ANSI tradicional, ya que se puede ejecutar en cualquier sistema operativo Windows de 32 bits. Puede compilar y ejecutar libremente con o sin Unicode en Windows Server 2003 y versiones posteriores, y Windows 2000 y versiones posteriores. Tenga en cuenta que APPUTIL siempre se compila con las mismas opciones que los otros ejemplos de código que se pueden compilar por separado. Esto es especialmente cierto para la opción **"Unicode = 1"** .

Puede usar un entorno de desarrollo integrado (IDE) de C++ de 32 bits instalado para compilar los ejemplos con los archivos make genéricos proporcionados. Para ello, es necesario que en el IDE se controlen los archivos make genéricos como archivos make ' externos '. Los archivos make proporcionados requieren una utilidad de creación compatible con NMAKE de Microsoft.

La mayoría de los IDE de C++ pueden reconocer estos archivos make como externos y, aun así, proporcionar muchas ventajas de edición-compilación-depuración del IDE. Por ejemplo, en Microsoft Visual Studio 97 o posterior, puede usar el menú Archivo abrir la opción del área de trabajo para generar un área de trabajo abriendo una copia con el nombre apropiado (por ejemplo, Exeskel. Mak) del archivo make de ejemplo de código Win32.

 

 




