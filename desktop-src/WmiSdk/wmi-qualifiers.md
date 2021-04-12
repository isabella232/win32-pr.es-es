---
description: WMI tiene varios tipos de calificadores de clase y propiedad. Los calificadores también pueden tener modificaciones de tipos.
ms.assetid: b889df69-327b-40d0-bbd7-a33d7924f3e1
ms.tgt_platform: multiple
title: Calificadores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90b14dc8f1f73571fc2c449e55c30034f86c2453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276111"
---
# <a name="wmi-qualifiers"></a>Calificadores WMI

WMI tiene varios tipos de [*calificadores*](gloss-q.md)de clase y propiedad. Los calificadores también pueden tener modificaciones de [*tipos*](gloss-f.md). En WMI se usan los siguientes tipos de calificadores y sabores.

El nombre de cada calificador aparece con su tipo de datos y un indicador de si el calificador se puede aplicar a una clase, instancia, propiedad o método. En el caso de los calificadores como la **Asociación** (descritos en [metacalificadores](meta-qualifiers.md)), hay una regla de uso implícita que también debe tener el calificador meta. Por ejemplo, la regla de uso implícita para los calificadores de **agregación** es que el calificador de **Asociación** también debe estar presente.



| Tipo de calificador                              | Descripción                                                                                                                           |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Dispositivo](meta-qualifiers.md)                 | Refina la definición de las meta-construcciones aclarando el uso real de una declaración de clase o propiedad.                          |
| [Opcional](optional-qualifiers.md)         | Aborda situaciones que no son comunes a todas las implementaciones compatibles con CIM.                                                                 |
| [Tipos de calificador](qualifier-flavors.md)  | Proporciona más información sobre un calificador, como si una clase derivada o una instancia pueden reemplazar el valor original del calificador. |
| [Estándar](standard-qualifiers.md)         | Admite las descripciones que todas las implementaciones compatibles con CIM deben controlar.                                                         |
| [Específico de WMI](wmi-specific-qualifiers.md) | Describe los calificadores específicos de WMI, como los calificadores de clase de contador de rendimiento.                                                   |



 

Para obtener más información sobre cómo aplicar calificadores a las clases de WMI, vea [Agregar un calificador](adding-a-qualifier.md). Para ver cómo examinar los calificadores de clases WMI existentes, consulte el código de ejemplo siguiente.

## <a name="example"></a>Ejemplo

El siguiente código de PowerShell, tomado de la [Galería de TechNet](https://Gallery.TechNet.Microsoft.Com/Get-WMI-Class-qualifiers-239970e7), describe cómo recuperar calificadores de una clase WMI.


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



 

 



