---
title: Función de tipo de tamaño (D2d1helper.h)
description: Crea una estructura de tamaño que almacena su ancho y alto con el tipo de datos especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Función de tipo de tamaño Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39d689d5f5c729e13385fc0d6d5b31baf96b141b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886986"
---
# <a name="sizelttypegt-function"></a>Función &lt; De tipo de &gt; tamaño

Crea una estructura de tamaño que almacena su ancho y alto con el tipo de datos especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Tipo      | Tipo de datos utilizado para almacenar el ancho y alto del tamaño. Los valores posibles son FLOAT y UINT32. |



 

## <a name="parameters"></a>Parámetros



| Parámetro | Descripción        |
|-----------|--------------------|
| width     | Ancho del tamaño.  |
| height    | Alto del tamaño. |



 

## <a name="return-value"></a>Valor devuelto

Tamaño que contiene el ancho y alto especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| para aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





