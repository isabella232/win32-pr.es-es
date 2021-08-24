---
title: Uso de un Moniker de sesión
description: La activación de sesión a sesión permite que un proceso de cliente active un proceso de servidor local en una sesión especificada.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fc5c65c3e2efd3e566a3fdde6982fefe5bb14fbefd98ca8abd335955b7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868855"
---
# <a name="using-a-session-moniker"></a>Uso de un Moniker de sesión

La activación de sesión a sesión permite que un proceso de cliente active un proceso de servidor local en una sesión especificada. Puede hacerlo por sesión mediante un moniker de sesión proporcionado por el sistema. Para obtener más información sobre cómo crear un moniker de sesión, vea Activación de sesión [a sesión con un Moniker de sesión.](session-to-session-activation-with-a-session-moniker.md)

En el ejemplo siguiente se muestra cómo activar un proceso de servidor local con el identificador de clase "10000013-0000-0000-0000-000000000001" en la sesión con el identificador de sesión 3.

En primer lugar, el ejemplo llama a [**la función CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca COM. A continuación, el ejemplo llama a [**CreateBindCtx para**](/windows/win32/api/objbase/nf-objbase-createbindctx) recuperar un puntero a una implementación de la [**interfaz IBindCtx.**](/windows/win32/api/objidl/nn-objidl-ibindctx) Este objeto almacena información sobre las operaciones de enlace de moniker; El puntero es necesario para llamar a métodos de la [**interfaz IMoniker.**](/windows/win32/api/objidl/nn-objidl-imoniker) A continuación, el ejemplo llama a la función [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para crear el moniker de sesión compuesta y, a continuación, al método [**IMoniker::BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para activar la conexión entre el cliente y el proceso de servidor, mediante el moniker de sesión recién creado. En este momento puede usar el puntero de interfaz para realizar las operaciones deseadas en el objeto . Por último, el ejemplo libera el contexto de enlace y llama a la [**función CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


```C++
// Initialize COM.

HRESULT hr = CoInitialize(NULL);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get interface pBindCtx.

IBindCtx* pBindCtx;
hr = CreateBindCtx(NULL, &pBindCtx);
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get moniker pMoniker.

OLECHAR string[] =
    L"Session:3!clsid:10000013-0000-0000-0000-000000000001";
ULONG ulParsed;
IMoniker* pMoniker;
hr = MkParseDisplayNameEx( pBindCtx,
                           string,
                           &ulParsed,
                           &pMoniker
                          );
if (FAILED(hr)) exit(0);  // Handle errors here.

// Get object factory pSessionTestFactory.

IUnknown* pSessionTestFactory;
hr = pMoniker->BindToObject( pBindCtx,
                             NULL,
                             IID_IUnknown,
                             (void**)&pSessionTestFactory
                            );
if (FAILED(hr)) exit(0);  // Handle errors here.

//
// Make, use, and destroy object here.
//
pSessionTestFactory->Release();
pSessionTestFactory = NULL;

pMoniker->Release();  // Release moniker.

pBindCtx->Release();  // Release interface.

CoUninitialize();  // Release COM.
```



Dado que "{class id of the class moniker}" también es una manera de dar nombre a un moniker de clase, puede usar la siguiente cadena para dar nombre al moniker compuesto (el moniker de sesión compuesto con el moniker de clase) en lugar del modo que se muestra en el ejemplo anterior.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Si el mismo usuario ha iniciado sesión en cada sesión durante una activación entre sesiones, puede activar correctamente cualquier proceso de servidor configurado para ejecutarse en el modo de activación RunAs Interactive User. Si distintos usuarios han iniciado sesión en cada sesión, el servidor debe llamar a la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer los derechos de usuario adecuados antes de que se pueda producir una activación y conexión correctas entre el cliente y el servidor. Una manera de lograrlo sería que el servidor implementara una interfaz [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada y pasara la implementación a **CoInitializeSecurity**. En cualquier caso, el usuario [](../com/launchpermission.md) cliente debe tener los permisos de inicio y acceso [**adecuados especificados**](../com/accesspermission.md) por la aplicación que se ejecuta en el servidor. Para obtener más información, [vea Seguridad en COM.](../com/security-in-com.md)

 

Para obtener más información sobre los monikers y monikers proporcionados por el sistema y los modos de activación, vea [Monikers](../com/monikers.md), la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) y [AppId Key](/windows/desktop/com/appid-key) en la documentación de COM del Kit de desarrollo de software de plataforma (SDK).

 

 