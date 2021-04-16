---
description: Inicializa la \_ biblioteca klib de AUX.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Función AuxKlibInitialize (AUX \_ klib. h)
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
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650104"
---
# <a name="auxklibinitialize-function"></a>AuxKlibInitialize función)

Inicializa la \_ biblioteca klib de AUX. Se debe llamar a esta función antes de que se pueda llamar a cualquier otra función de la biblioteca.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en NTSTATUS. h, que está disponible en el WDK.

## <a name="remarks"></a>Observaciones

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuible<br/> | Biblioteca de API auxiliar de Windows versión 1,0 o posterior<br/>                            |
| Encabezado<br/>          | <dl> <dt>AUX \_ klib. h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>AUX \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibQueryModuleInformation**](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




