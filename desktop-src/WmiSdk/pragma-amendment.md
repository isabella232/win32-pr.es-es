---
description: Indica al compilador MOF que separe un archivo MOF en versiones independientes del lenguaje y específicas del idioma.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: modificación de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811425"
---
# <a name="pragma-amendment"></a>modificación de pragma

El comando de preprocesador de **modificación de pragma** indica al compilador de MOF que separe un archivo MOF en versiones independientes del idioma y del idioma. El archivo MOF específico del idioma mueve los calificadores modificados a un espacio de nombres para una configuración regional específica. Después, debe compilar los archivos MOF específicos del idioma y del idioma independiente para almacenar la información de clase en el repositorio WMI.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo crear un archivo MOF que contenga calificadores modificados. Después, puede compilar el código MOF con el siguiente comando:

**MOFCOMP** **-MOF: Lnmof. mof** **-MFL: Lsmof. MFL** **Mastermof. mof**

El comando indica al compilador MOF que genere dos archivos MOF del archivo Mastermof. mof original. El compilador MOF genera una versión independiente del lenguaje del archivo MOF, denominada Lnmof. mof, con todos los elementos específicos del idioma que se han quitado. El compilador también crea un segundo archivo MOF específico del lenguaje denominado Lsmof. MFL que contiene solo los elementos que se deben localizar.

> [!Note]  
> Cuando divida un archivo MOF con el calificador de **modificación** o el comando **pragma de modificación** , debe especificar las opciones **-MOF** y **-MFL** . De lo contrario, el compilador no genera ningún archivo de salida. A continuación, debe compilar los dos archivos de salida para que la información de la clase esté disponible en WMI.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




