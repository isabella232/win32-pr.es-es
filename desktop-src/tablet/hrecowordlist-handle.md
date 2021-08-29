---
description: Un identificador HRECOWORDLIST se usa para administrar una lista de palabras que se asocia a un contexto de reconocedor. Use una lista de palabras para mejorar los resultados del reconocimiento.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Identificador HRECOWORDLIST (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7384873f562627f54326cfca78883c9f3a02351dad1df0bf45a23b61b03c167d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967574"
---
# <a name="hrecowordlist-handle"></a>Identificador HRECOWORDLIST

Un **identificador HRECOWORDLIST** se usa para administrar una lista de palabras que se asocia a un contexto de reconocedor. Use una lista de palabras para mejorar los resultados del reconocimiento.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Comentarios

La función siguiente usa **hrecowordlist**.



| Función                                         | Descripción                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Agrega una o varias palabras a la lista de palabras.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Destruye la lista de palabras actual.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Crea una lista de palabras.<br/>                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetWordList (Función)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




