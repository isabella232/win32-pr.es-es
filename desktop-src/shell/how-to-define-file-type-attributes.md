---
description: Definición de atributos de tipo de archivo en el Registro.
ms.assetid: EE35E3E7-0573-45CA-A21A-89E50B86487D
title: Definición de atributos de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0a89f5770b55521ccdf51859bdde69ed58d05f864385e46f1d76e482319c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223579"
---
# <a name="how-to-define-file-type-attributes"></a>Definición de atributos de tipo de archivo

La asignación de atributos de tipo de archivo a un ProgID asociado le permite controlar algunos aspectos del comportamiento del tipo de archivo. Antes de Windows Vista, estos atributos podían permitirle limitar la medida en  que el usuario podría usar la pestaña de propiedades Opciones de carpeta para modificar varios aspectos del tipo de archivo, como su icono o verbos.

Los atributos de tipo de archivo son marcas binarias especificadas como **valores REG \_ DWORD** o **REG \_ BINARY** en la subclave ProgID asociada del tipo de archivo.

Para asignar atributos para un tipo de archivo, siga estos pasos.

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Agregue una entrada EditFlags a la subclave ProgID asociada del tipo de archivo.

### <a name="step-2"></a>Paso 2:

Establezca la entrada en el valor de atributo adecuado.

En el ejemplo siguiente se muestran los atributos \_ FTA NoRemove (0x00000010) y FTA NoNewVerb (0x00000020) establecidos para el tipo de \_ archivo .myp.

```
HKEY_CLASSES_ROOT
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
      EditFlags = 0x00000030
```

## <a name="remarks"></a>Comentarios

Las marcas se pueden combinar con un OPERADOR lógico para formar el valor de atributo único.

Para obtener una lista de posibles atributos de tipo de archivo y sus valores hexadecimales, y más detalles sobre cómo recuperar y establecer estos valores mediante programación, vea [**FILETYPEATTRIBUTEFLAGS**](/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags).

 

 



