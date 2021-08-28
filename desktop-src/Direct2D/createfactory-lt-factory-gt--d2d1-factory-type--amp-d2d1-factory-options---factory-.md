---
title: Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
description: Crea un objeto de generador que se puede usar para crear recursos de Direct2D. | Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Función Direct2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory )
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08562269bc682b9138f2413c33b41ad3d2aebf7d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885085"
---
# <a name="d2d1createfactoryltfactorygtd2d1_factory_typed2d1_factory_optionsfactory-function"></a>Función D2D1CreateFactory &lt; Factory &gt; (D2D1 \_ FACTORY \_ TYPE,D2D1 \_ FACTORY OPTIONS \_&,Factory \* \* )

Crea un objeto de generador que se puede usar para crear recursos de Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                 |
|-----------|-------------------------------------------------------------|
| *Fábrica* | Tipo de [**ID2D1Factory que**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) se creará. |



 

## <a name="parameters"></a>Parámetros



| Parámetro        | Descripción                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | El modelo de subprocesos del generador y los recursos que crea.                |
| *factoryOptions* | Nivel de detalle proporcionado a la capa de depuración.                            |
| *fábrica*        | Cuando este método devuelve un resultado, contiene la dirección de un puntero al nuevo generador. |



 

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista \[ \| para aplicaciones para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Encabezado<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

