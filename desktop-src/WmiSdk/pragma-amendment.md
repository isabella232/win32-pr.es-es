---
description: Dirige al compilador MOF para separar un archivo MOF en versiones independientes del lenguaje y específicas del lenguaje.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: modificación pragma
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
ms.openlocfilehash: 6204ac7f3cd78de8d2eed9740fc165475d387e65284bcbf6be1ea10ed91a0926
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992735"
---
# <a name="pragma-amendment"></a>modificación pragma

El comando pragma amendment preprocessor (Preprocesador de modificación **pragma)** ordena al compilador MOF que separe un archivo MOF en versiones independientes del lenguaje y específicas del lenguaje. El archivo MOF específico del lenguaje mueve los calificadores modificados a un espacio de nombres para una configuración regional específica. A continuación, compile los archivos MOF específicos y neutrales del lenguaje para almacenar información de clase en el repositorio WMI.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo crear un archivo MOF que contiene calificadores modificados. A continuación, puede compilar el código MOF con el siguiente comando:

**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**

El comando indica al compilador MOF que produzca dos archivos MOF a partir del archivo Mastermof.mof original. El compilador MOF genera una versión neutra del lenguaje del archivo MOF, denominada Lnmof.mof, con todos los elementos específicos del idioma quitados. El compilador también crea un segundo archivo MOF específico del lenguaje denominado Lsmof.mfl que contiene solo los elementos que debe encontrar.

> [!Note]  
> Al dividir un archivo MOF  con el calificador de modificación o el comando **pragma amendment,** debe especificar las opciones **-MOF** **y -MFL.** De lo contrario, el compilador no genera ningún archivo de salida. A continuación, debe compilar los dos archivos de salida para que la información de clase esté disponible para WMI.

 


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



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




