---
description: En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funciones DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f8c10951c63e14656fa967693145444c5d5fbffd96a2b11fa9ae4201ac89ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821089"
---
# <a name="dll-functions"></a>Funciones DLL

En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.

Un archivo DLL debe implementar las siguientes funciones para que se pueda registrar, anular el registro y cargarse en la memoria.

-   [*DllMain:*](/windows/desktop/Dlls/dllmain)punto de entrada de DLL. El nombre *DllMain es* un marcador de posición para el nombre de la función definida por la biblioteca. La DirectShow utiliza el nombre **DllEntryPoint**. Para obtener más información, consulte Platform SDK.
-   [**DllGetClassObject:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject)crea una instancia de generador de clases. Se describe en las secciones anteriores.
-   [**DllCanUnloadNow:**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow)consulta si el archivo DLL se puede descargar de forma segura.
-   [**DllRegisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver)crea entradas del Registro para el archivo DLL.
-   [**DllUnregisterServer:**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver)quita las entradas del Registro para el archivo DLL.

De estas, las tres primeras se implementan mediante DirectShow. Si la plantilla de generador proporciona una función de inicialización en la variable miembro [**m \_ lpfnInit,**](cfactorytemplate-m-lpfninit.md) se llama a esa función desde dentro de la función de punto de entrada dll. Para obtener más información sobre cuándo el sistema llama a la función de punto de entrada dll, [*vea DllMain*](/windows/desktop/Dlls/dllmain).

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



Sin embargo, [**en DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) puede personalizar el proceso de registro según sea necesario. Si el archivo DLL contiene un filtro, es posible que tenga que realizar algún trabajo adicional. Para obtener más información, [vea How to Register DirectShow Filters](how-to-register-directshow-filters.md).

En el archivo de definición de módulo (.def), exporte todas las funciones DLL excepto la función de punto de entrada. A continuación se muestra un archivo .def de ejemplo:


```C++
EXPORTS
    DllGetClassObject PRIVATE
    DllCanUnloadNow PRIVATE
    DllRegisterServer PRIVATE
    DllUnregisterServer PRIVATE
```



Puede registrar el archivo DLL mediante la utilidad Regsvr32.exe.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un archivo DLL DirectShow filtro de archivos](how-to-create-a-dll.md)
</dt> </dl>

 

 
