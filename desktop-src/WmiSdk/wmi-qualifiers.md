---
description: WMI tiene varios tipos de calificadores de clase y propiedad. Los calificadores también pueden tener la modificación de los flavors.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Calificadores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf51888592949aadefec7c864dc0a24df6a4fa68f6fb34c8e3cda880da6873
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502815"
---
# <a name="wmi-qualifiers"></a>Calificadores WMI

WMI tiene varios tipos de calificadores de [*clase y propiedad*](gloss-q.md). Los calificadores también pueden tener la modificación [*de los flavors*](gloss-f.md). En WMI se usan los siguientes tipos de calificadores y tipos.

El nombre de cada calificador aparece con su tipo de datos y un indicador de si el calificador se puede aplicar a una clase, instancia, propiedad o método. Para calificadores como **Association** (que se describe en [Meta Qualifiers),](meta-qualifiers.md)hay una regla de uso implícita que el meta calificador también debe estar presente. Por ejemplo, la regla de uso implícito para los calificadores **de agregación** es que el calificador **association** también debe estar presente.



| Tipo de calificador                              | Descripción                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Meta](meta-qualifiers.md)                 | Refina la definición de meta construcciones aclarando el uso real de una declaración de clase o propiedad.                          |
| [Opcional](optional-qualifiers.md)         | Aborda situaciones que no son comunes a todas las implementaciones compatibles con CIM.                                                                 |
| [Flavors de calificador](qualifier-flavors.md)  | Proporciona más información sobre un calificador, como si una clase o instancia derivada puede invalidar el valor original del calificador. |
| [Estándar](standard-qualifiers.md)         | Admite las descripciones que deben controlar todas las implementaciones compatibles con CIM.                                                         |
| [Específico de WMI](wmi-specific-qualifiers.md) | Describe calificadores específicos de WMI, como calificadores de clase de contador de rendimiento.                                                   |



 

Para obtener más información sobre cómo aplicar calificadores a las clases WMI, vea [Agregar un calificador](adding-a-qualifier.md). Para ver cómo examinar calificadores en clases WMI existentes, vea el código de ejemplo siguiente.

## <a name="example"></a>Ejemplo

El siguiente código de PowerShell, tomado de la galería [de TechNet,](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7)describe cómo recuperar calificadores de una clase WMI.


```PowerShell
Function Get-WMIClassesWithQualifiers 
{ 
 Param([string]$qualifier = "dynamic", 
  [string]$namespace = "root\cimv2") 
 $classes = Gwmi -list -namespace $namespace 
 foreach($class in $classes) 
 { 
  $query = "select * from meta_class where __this isa ""$($class.name)"" " 
  $a = gwmi -Query $query -Namespace $namespace |  
  select -Property __class, qualifiers 
   if($a.qualifiers | % { $_ | ? { $_.name -match "$qualifier" }}) 
    { $a.__class } 
  } #end foreach $class 
} 
```



 

 



