---
description: En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funciones DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061673"
---
# <a name="dll-functions"></a>Funciones DLL

En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.

Un archivo DLL debe implementar las siguientes funciones para que se pueda registrar, anular el registro y cargarse en la memoria.

-   [*DllMain:*](/windows/desktop/Dlls/dllmain)el punto de entrada del archivo DLL. El nombre *DllMain es* un marcador de posición para el nombre de la función definida por la biblioteca. La DirectShow utiliza el nombre **DllEntryPoint**. Para obtener más información, consulte el SDK de plataforma.
-   [**DllGetClassObject:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)crea una instancia de generador de clases. Se describe en las secciones anteriores.
-   [**DllCanUnloadNow:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)consulta si el archivo DLL se puede descargar de forma segura.
-   [**DllRegisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)crea entradas del Registro para el archivo DLL.
-   [**DllUnregisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)quita las entradas del Registro para el archivo DLL.

De estas, las tres primeras se implementan mediante DirectShow. Si la plantilla de generador proporciona una función de inicialización en la variable miembro [**m \_ lpfnInit,**](cfactorytemplate-m-lpfninit.md) se llama a esa función desde dentro de la función de punto de entrada de DLL. Para obtener más información sobre cuándo el sistema llama a la función de punto de entrada dll, vea [*DllMain*](/windows/desktop/Dlls/dllmain).

Debe implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer,**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)pero DirectShow proporciona una función denominada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que realiza el trabajo necesario. El componente puede simplemente encapsular esta función, como se muestra en el ejemplo siguiente:


```C++
STDAPI DllRegisterServer()
{
    return AMovieDllRegisterServer2( TRUE );
}

STDAPI DllUnregisterServer()
{
    return AMovieDllRegisterServer2( FALSE );
}
```



Sin embargo, [**en DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) puede personalizar el proceso de registro según sea necesario. Si el archivo DLL contiene un filtro, es posible que deba realizar algún trabajo adicional. Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

En el archivo module-definition (.def), exporte todas las funciones DLL excepto la función de punto de entrada. A continuación se muestra un archivo .def de ejemplo:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Puede registrar el archivo DLL mediante la utilidad Regsvr32.exe .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un archivo DIRECTSHOW dll de filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 
