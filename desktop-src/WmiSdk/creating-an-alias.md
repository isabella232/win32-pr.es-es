---
description: Un alias de WMI es una referencia simbólica en una clase o en una instancia de clase ubicada en otra parte de un archivo Managed Object Format (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Crear un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465896"
---
# <a name="creating-a-wmi-alias"></a>Crear un alias WMI

Un [*alias*](gloss-a.md) de WMI es una referencia simbólica en una clase o una instancia de clase ubicada en otra parte de un archivo Managed Object Format (MOF). El compilador de MOF usa alias para establecer referencias entre clases e instancias. El compilador resuelve los alias en las clases a las que hacen referencia, por lo que los nombres de alias no están disponibles en el código compilado. Como resultado, las aplicaciones cliente no pueden hacer referencia a clases mediante alias.

> [!Note]  
> WMI admite referencias de reenvío, pero no alias circulares.

 

Un alias solo tiene ámbito dentro del archivo MOF en el que se declara el alias. Por lo tanto, normalmente se usa un alias como acceso directo a una ruta de acceso de objeto larga.

**Para definir un alias**

1.  Agregue la frase "as $*aliasname"* a la declaración de instancia o clase.
2.  Los nombres de alias siguen las mismas reglas que los nombres de instancia y clase, excepto que los nombres de alias deben comenzar con un signo de dólar ($). Los caracteres de subrayado pueden aparecer en un nombre de alias después del carácter inicial.

En el ejemplo de código siguiente se describe cómo usar un alias en una definición de clase.

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

En los ejemplos de código siguientes se describe cómo usar un alias como referencia simbólica a una ruta de acceso de objeto. En estos ejemplos se declaran dos clases para describir un disco: la clase Disk para indicar la letra de unidad y la clase DiskRef para indicar la ruta de acceso del disco. Se define un alias para la instancia de clase Disk. Este alias se usa como valor de la propiedad PathToDisk en la instancia de DiskRef.

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 



