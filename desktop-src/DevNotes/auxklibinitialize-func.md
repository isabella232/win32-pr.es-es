---
description: Inicializa la biblioteca \_ Auxiliar klib.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Función AuxKlibInitialize (Aux \_ klib.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: f35d2d17d581d17a6d89a7bc10d185a67a5fb0b695a29492922f5950241f2ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654885"
---
# <a name="auxklibinitialize-function"></a>Función AuxKlibInitialize

Inicializa la biblioteca \_ Auxiliar klib. Se debe llamar a esta función para poder llamar a cualquier otra función de la biblioteca.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es STATUS \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en Ntstatus.h, que está disponible en wdk.

## <a name="remarks"></a>Comentarios

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca de API auxiliar versión 1.0 o posterior<br/>                            |
| Header<br/>          | <dl> <dt>Aux \_ klib.h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>Aux \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




