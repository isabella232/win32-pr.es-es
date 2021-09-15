---
description: La creación de definiciones de clase localizadas es un proceso de tres pasos.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Crear definiciones de clase localizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575385"
---
# <a name="creating-localized-class-definitions"></a>Crear definiciones de clase localizadas

La creación de definiciones de clase localizadas es un proceso de tres pasos. Para empezar, escriba código MOF que defina las clases, incluidos todos los calificadores que deben localizarse. Este archivo original se denomina archivo "MOF maestro" porque contiene todos los calificadores y propiedades que definen la clase.

A continuación, use [el compilador MOF](mofcomp.md) para crear las versiones neutras del lenguaje y específicas del lenguaje del archivo MOF. El compilador MOF coloca la descripción de clase básica en un nuevo archivo MOF y crea una versión localizada del archivo MOF que contiene solo las propiedades y calificadores que deben localizarse. Aunque las versiones específicas del idioma y las versiones neutras del lenguaje del archivo MOF pueden tener el mismo nombre de archivo, debe usar una extensión de nombre de archivo .mfl para indicar que el archivo contiene información localizada. Si es necesario, puede encontrar el archivo .mfl en otras configuraciones regionales. El almacenamiento de las definiciones de clase en el repositorio CIM requiere un paso adicional de uso del compilador MOF para compilar los archivos MOF específicos del lenguaje y del lenguaje neutros.

En los pasos siguientes se describe cómo crear y almacenar una definición de clase localizada.

**Para crear y almacenar una definición de clase localizada**

1.  Cree el archivo MOF maestro que define las clases que desea localizar.

    Guarde este código MOF en un archivo denominado Mastermof.mof.

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  Cree versiones del archivo MOF sin idioma y específicas del idioma mediante la compilación del archivo MasterMOF.mof.

    Escriba el siguiente comando en un símbolo del sistema para compilar el archivo MasterMOF.mof.

    **mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS \_ 409 Mastermof.mof**

3.  Compile los archivos de lenguaje neutro (Lnmof.mof) y específicos del lenguaje (Lsmof.mfl) y almacene la información de clase en el repositorio CIM.

    Escriba los siguientes comandos en un símbolo del sistema para almacenar la información de clase en el repositorio CIM.

    **Mofcomp Lnmof.mof**

    **Mofcomp Lsmof.mfl**

    Después de compilar estos archivos, tendrá una definición de clase neutra del lenguaje en el espacio de nombres de prueba raíz y una definición de clase localizada en el espacio de nombres \\ \\ \\ ms \_ 409 de la prueba raíz. Para obtener más información sobre la compilación de archivos MOF localizados, vea [Compilar archivos MOF localizados.](compiling-localized-mof-files.md)

 

 



