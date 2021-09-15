---
description: Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Clase InkWordList (Msyecciónut.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359640"
---
# <a name="inkwordlist-class"></a>InkWordList (clase)

Representa una lista de palabras que se pueden usar para mejorar el resultado del reconocimiento.

**InkWordList** tiene estos tipos de miembros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)

### <a name="interfaces"></a>Interfaces

La **clase InkWordList** define estas interfaces.



| Interfaz        | Descripción                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Este objeto implementa la **interfaz COM IInkWordList.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase InkWordList** tiene estos métodos.



| Método                                       | Descripción                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Agrega una sola palabra a **InkWordList.**<br/>                   |
| [**Merge**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Combina otro **objeto InkWordList** en en **este objeto InkWordList.**<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Quita una sola palabra de **un objeto InkWordList.**<br/>                |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Msgniut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Constantes factoid](factoid-constants.md)
</dt> <dt>

[**InkRecognizerContext (clase)**](inkrecognizercontext-class.md)
</dt> </dl>

 

