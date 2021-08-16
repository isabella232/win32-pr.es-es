---
title: Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
description: Crea un objeto de generador que se puede usar para crear recursos de Direct2D. | Función D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af5635a6f996ea6cd3af2c3b3022efa054cd27605430c8230143980e00b9abbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826474"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a>Función D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,Factory \* \* )

Crea un objeto de generador que se puede usar para crear recursos de Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Parámetros de plantilla



| Parámetro | Descripción                                                 |
|-----------|-------------------------------------------------------------|
| *Fábrica* | Tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se creará. |



 

## <a name="parameters"></a>Parámetros



| Parámetro     | Descripción                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | El modelo de subprocesos del generador y los recursos que crea.                |
| *fábrica*     | Cuando este método devuelve un resultado, contiene la dirección de un puntero al nuevo generador. |



 

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un generador.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7, Windows Vista con SP2 y Platform Update for Windows Vista \[ desktop apps \| UWP apps\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 y Actualización de plataforma para aplicaciones de escritorio de Windows Server 2008 aplicaciones \[ \| para UWP\]<br/> |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| Archivo DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

