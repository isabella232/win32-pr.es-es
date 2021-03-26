---
description: Definir atributos de tipo de archivo en el registro.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Cómo definir atributos de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7844c65191d6513a06625a28c47accd3df5cc82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909549"
---
# <a name="how-to-define-file-type-attributes"></a>Cómo definir atributos de tipo de archivo

La asignación de atributos de tipo de archivo a un ProgID asociado permite controlar algunos aspectos del comportamiento del tipo de archivo. Antes de Windows Vista, estos atributos podían permitirle limitar el grado en el que el usuario podía usar la pestaña de propiedades de **Opciones de carpeta** para modificar diversos aspectos del tipo de archivo, como su icono o verbos.

Los atributos de tipo de archivo son marcas binarias especificadas como valores **reg \_ DWORD** o **reg \_ Binary** en la subclave ProgID asociada del tipo de archivo.

Para asignar atributos para un tipo de archivo, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Agregue una entrada marcas a la subclave ProgID asociada del tipo de archivo.

### <a name="step-2"></a>Paso 2:

Establezca la entrada en el valor de atributo adecuado.

En el ejemplo siguiente se muestran los \_ atributos FTA noremove (0x00000010) y FTA \_ NoNewVerb (0x00000020) establecidos para el tipo de archivo. MYP.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Observaciones

Las marcas se pueden combinar con un operador lógico OR para formar el valor de atributo único.

Para obtener una lista de los posibles atributos de tipo de archivo y sus valores hexadecimales, y más detalles sobre cómo recuperar y establecer estos valores mediante programación, vea [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



