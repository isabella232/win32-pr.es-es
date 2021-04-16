---
description: Un identificador HRECOWORDLIST se usa para administrar una lista de palabras que se adjunta a un contexto de reconocedor. Use una lista de palabras para mejorar los resultados del reconocimiento.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Identificador de HRECOWORDLIST (Resumen. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542123"
---
# <a name="hrecowordlist-handle"></a>Identificador de HRECOWORDLIST

Un identificador **HRECOWORDLIST** se usa para administrar una lista de palabras que se adjunta a un contexto de reconocedor. Use una lista de palabras para mejorar los resultados del reconocimiento.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Observaciones

La siguiente función usa un **HRECOWORDLIST**.



| Función                                         | Descripción                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Agrega una o más palabras a la lista de palabras.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Destruye la lista de palabras actual.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Crea una lista de palabras.<br/>                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Resumen. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SetWordList función)**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




