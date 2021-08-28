---
title: Creación de la tabla de interfaz global
description: Creación de la tabla de interfaz global
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836cc5507ac9b8e7cccd6e9dc8fd8c2d71e1a23419945ecc01d35b3978940124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793775"
---
# <a name="creating-the-global-interface-table"></a>Creación de la tabla de interfaz global

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
> Al crear el objeto de tabla de interfaz global mediante la llamada anterior, es necesario vincular a la biblioteca uuid.lib. Esto resolverá los símbolos externos CLSID \_ StdGlobalInterfaceTable e IID \_ IGlobalInterfaceTable.

 

Hay una sola instancia de la tabla de interfaz global por proceso, por lo que todas las llamadas a esta función de un proceso devuelven la misma instancia.

Después de llamar a la función [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) registre la interfaz desde el apartamento en el que reside con una llamada al [**método RegisterInterfaceInGlobal.**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) Este método proporciona una cookie que identifica la interfaz y su ubicación. Un apartamento que busca un puntero a esta interfaz llama al método [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) con esta cookie y, a continuación, la implementación proporciona un puntero de interfaz al apartamento que realiza la llamada. Para revocar el registro global de la interfaz, cualquier apartamento puede llamar al [**método RevokeInterfaceFromGlobal.**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal)

Un ejemplo sencillo de uso de [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) sería cuando se quiere pasar un puntero de interfaz en un objeto en un apartamento de un solo subproceso (STA) a un subproceso de trabajo de otro apartamento. En lugar de tener que serializar en una secuencia y pasar la secuencia al subproceso de trabajo como un parámetro de subproceso, **IGlobalInterfaceTable** permite pasar simplemente una cookie.

Al registrar la interfaz en la tabla de interfaz global, obtiene una cookie que puede usar en lugar de pasar el puntero real (siempre que necesite pasar el puntero), ya sea a un parámetro no de método que vaya a otro apartamento (como parámetro a [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) a través de [**CreateThread)**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)o a la memoria en proceso accesible fuera de su apartamento.

Es necesario tener cuidado porque el uso de interfaces globales supone una carga adicional para el programador de administrar problemas como condiciones de carrera y exclusión mutua, que están asociados al acceso al estado global desde varios subprocesos simultáneamente.

COM proporciona una implementación estándar de la [**interfaz IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Se recomienda encarecidamente usar esta implementación estándar porque proporciona una funcionalidad completa segura para subprocesos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cuándo usar la tabla de interfaz global](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 