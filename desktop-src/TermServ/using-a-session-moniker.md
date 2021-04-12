---
title: Uso de un moniker de sesión
description: La activación de sesión a sesión permite que un proceso de cliente Active un proceso de servidor local en una sesión especificada.
ms.assetid: de4967b6-6a53-4888-84f9-3fa29cbebe34
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700d251aa1136747529b66b975d4cbedf9b14dcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359323"
---
# <a name="using-a-session-moniker"></a>Uso de un moniker de sesión

La activación de sesión a sesión permite que un proceso de cliente Active un proceso de servidor local en una sesión especificada. Puede hacerlo por sesión mediante un moniker de sesión proporcionado por el sistema. Para obtener más información sobre cómo crear un moniker de sesión, consulte [activación de sesión en sesión con un moniker](session-to-session-activation-with-a-session-moniker.md)de sesión.

En el ejemplo siguiente se muestra cómo activar un proceso de servidor local con el ID. de clase "10000013-0000-0000-0000-000000000001" en la sesión con el identificador de sesión 3.

En primer lugar, el ejemplo llama a la función [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) para inicializar la biblioteca com. Después, el ejemplo llama a [**CreateBindCtx**](/windows/win32/api/objbase/nf-objbase-createbindctx) para recuperar un puntero a una implementación de la interfaz [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) . Este objeto almacena información sobre las operaciones de enlace de moniker; el puntero es necesario para llamar a los métodos de la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) . A continuación, el ejemplo llama a la función [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) para crear el moniker de sesión compuesto y, a continuación, el método [**IMoniker:: BindToObject**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) para activar la conexión entre el cliente y el proceso de servidor, mediante el moniker de sesión recién creado. En este momento puede usar el puntero de interfaz para realizar las operaciones deseadas en el objeto. Finalmente, el ejemplo libera el contexto de enlace y llama a la función [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


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



Como "{ID. de clase de la clase moniker}" es también una forma de asignar un nombre a un moniker de clase, puede usar la cadena siguiente para asignar un nombre al moniker compuesto (el moniker de la sesión compuesto por el moniker de la clase) en lugar de la forma que se muestra en el ejemplo anterior.

``` syntax
OLECHAR string[] = 
    L"Session:3!{0000031A-0000-0000-C000-000000000046}:
    10000013-0000-0000-0000-000000000001";
```

> [!Note]  
> Si el mismo usuario ha iniciado sesión en cada sesión durante una activación entre sesiones, puede activar correctamente cualquier proceso de servidor configurado para ejecutarse en el modo de activación de usuario interactivo de runas. Si varios usuarios inician sesión en cada sesión, el servidor debe llamar a la función [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para establecer los derechos de usuario adecuados antes de que se pueda realizar una activación y una conexión correctas entre el cliente y el servidor. Una manera de lograr esto sería que el servidor implementara una interfaz [**IAccessControl**](/windows/win32/api/iaccess/nn-iaccess-iaccesscontrol) personalizada y pasara la implementación a **CoInitializeSecurity**. En cualquier caso, el usuario del cliente debe tener los permisos de [**Inicio**](../com/launchpermission.md) y [**acceso**](../com/accesspermission.md) adecuados especificados por la aplicación que se ejecuta en el servidor. Para obtener más información, vea [seguridad en com](../com/security-in-com.md).

 

Para obtener más información acerca de los monikers y los monikers proporcionados por el sistema y los modos de activación, consulte [monikers](../com/monikers.md), la interfaz [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) y la [clave AppID](/windows/desktop/com/appid-key) en la documentación de com del kit de desarrollo de software (SDK) de la plataforma.

 

 