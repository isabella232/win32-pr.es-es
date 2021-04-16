---
description: En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.
ms.assetid: cb935c26-2dc9-4ab3-810d-b63f1018a62a
title: Funciones DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b6d1b15df86cf3d7a2eb81080ec02b02a868f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105651439"
---
# <a name="dll-functions"></a>Funciones DLL

En este tema se describe cómo implementar un componente como una biblioteca de vínculos dinámicos (DLL) en Microsoft DirectShow.

Un archivo DLL debe implementar las funciones siguientes para que se pueda registrar, anular el registro y cargar en la memoria.

-   [*DllMain*](/windows/desktop/Dlls/dllmain): el punto de entrada de dll. El nombre *DllMain* es un marcador de posición para el nombre de la función definida por la biblioteca. La implementación de DirectShow usa el nombre **DllEntryPoint**. Para obtener más información, vea el SDK de la plataforma.
-   [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject): crea una instancia de generador de clases. Se describe en las secciones anteriores.
-   [**DllCanUnloadNow**](/windows/desktop/api/combaseapi/nf-combaseapi-dllcanunloadnow): consulta si el archivo dll se puede descargar de forma segura.
-   [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver): crea entradas del registro para el archivo dll.
-   [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver): quita las entradas del registro para el archivo dll.

De ellos, DirectShow implementa los tres primeros. Si la plantilla de fábrica proporciona una función de inicialización en la variable miembro [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md) , se llama a esa función desde dentro de la función de punto de entrada del archivo dll. Para obtener más información sobre cuándo el sistema llama a la función de punto de entrada de DLL, vea [*DllMain*](/windows/desktop/Dlls/dllmain).

Debe implementar [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver), pero DirectShow proporciona una función denominada [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) que realiza el trabajo necesario. El componente puede ajustar simplemente esta función, tal y como se muestra en el ejemplo siguiente:


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



Sin embargo, en [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) y [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) , puede personalizar el proceso de registro según sea necesario. Si el archivo DLL contiene un filtro, puede que tenga que realizar algún trabajo adicional. Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).

En el archivo de definición de módulo (. def), exporte todas las funciones DLL excepto la función de punto de entrada. A continuación se encuentra un archivo. def de ejemplo:


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

[Cómo crear un archivo DLL de filtro de DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
