---
title: Función gluNewTess (Glu.h)
description: La función gluNewTess crea un objeto de teselación.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- Función gluNewTess OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271975"
---
# <a name="glunewtess-function"></a>función gluNewTess

La **función gluNewTess** crea un objeto de teselación.

## <a name="syntax"></a>Sintaxis


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="remarks"></a>Observaciones

La **función gluNewTess** crea y devuelve un puntero a un nuevo objeto de teselación. Haga referencia a este objeto al llamar a funciones de teselación. Un valor devuelto de cero significa que no hay suficiente memoria para asignar al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





