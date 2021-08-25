---
title: Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
description: Crea un objeto de generador que se puede usar para crear recursos de Direct2D. | Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function Direct2D
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
ms.openlocfilehash: 34cbe566b139ebd873e8e9895aa21307113be9632b2045d40c099f52f49fc574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824695"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>Función D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,D2D1 \_ FACTORY OPTIONS \_&,Factory \* \* )

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
| *fábrica*        | El resultado que devuelve este método contiene la dirección de un puntero al nuevo generador. |



 

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Actualización de plataforma para aplicaciones de escritorio Windows Vista aplicaciones \[ \| para UWP\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

