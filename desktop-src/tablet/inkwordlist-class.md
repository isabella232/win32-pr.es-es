---
description: Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Clase InkWordList (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707147"
---
# <a name="inkwordlist-class"></a>Clase InkWordList

Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.

**InkWordList** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

La clase **InkWordList** define estas interfaces.



| Interfaz        | Descripción                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Este objeto implementa la interfaz com **IInkWordList** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **InkWordList** tiene estos métodos.



| Método                                       | Descripción                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Agrega una sola palabra a **InkWordList**.<br/>                   |
| [**Sin**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Combina otro **InkWordList** con en este **InkWordList**.<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Quita una sola palabra de un **InkWordList**.<br/>                |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad de la propiedad de palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Constantes de Factoid](factoid-constants.md)
</dt> <dt>

[**Clase InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

