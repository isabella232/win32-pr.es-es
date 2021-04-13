---
title: Crear la tabla de interfaz global
description: Crear la tabla de interfaz global
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421485"
---
# <a name="creating-the-global-interface-table"></a>Crear la tabla de interfaz global

Use la siguiente llamada para crear el objeto de tabla de interfaz global y obtener un puntero a [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> Al crear el objeto de tabla de interfaz global mediante la llamada anterior, es necesario vincularlo a la biblioteca UUID. lib. Esto resolverá los símbolos externos CLSID \_ StdGlobalInterfaceTable y IID \_ IGlobalInterfaceTable.

 

Hay una única instancia de la tabla de interfaz global por proceso, por lo que todas las llamadas a esta función en un proceso devuelven la misma instancia.

Después de la llamada a la función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) , registre la interfaz desde el apartamento en el que reside con una llamada al método [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) . Este método proporciona una cookie que identifica la interfaz y su ubicación. Un contenedor que busca un puntero a esta interfaz llama entonces al método [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con esta cookie y, a continuación, la implementación proporciona un puntero de interfaz al apartamento que realiza la llamada. Para revocar el registro global de la interfaz, cualquier apartamento puede llamar al método [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .

Un ejemplo sencillo del uso de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) sería cuando desea pasar un puntero de interfaz a un objeto de un contenedor uniproceso (STA) a un subproceso de trabajo de otro apartamento. En lugar de tener que calcular las referencias en una secuencia y pasar la secuencia al subproceso de trabajo como un parámetro de subproceso, **IGlobalInterfaceTable** permite simplemente pasar una cookie.

Al registrar la interfaz en la tabla de interfaz global, obtiene una cookie que puede usar en lugar de pasar el puntero real (siempre que necesite pasar el puntero), ya sea a un parámetro que no sea de método que vaya a otro apartamento (como parámetro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) a través de [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) o a la memoria en proceso accesible fuera del apartamento.

Se requiere cuidado porque el uso de interfaces globales impone la carga adicional en el programador de la administración de problemas, como condiciones de carrera y exclusión mutua, que están asociados a tener acceso al estado global desde varios subprocesos simultáneamente.

COM proporciona una implementación estándar de la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Se recomienda encarecidamente que use esta implementación estándar, ya que proporciona una funcionalidad completa de subprocesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cuándo usar la tabla de interfaz global](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 