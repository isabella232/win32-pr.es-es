---
description: Los proveedores pueden llamar a métodos implementados por WMI desde dentro de sus implementaciones de método.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Realizar llamadas a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317679"
---
# <a name="making-calls-to-wmi"></a>Realizar llamadas a WMI

Los proveedores pueden llamar a métodos implementados por WMI desde dentro de sus implementaciones de método. Sin embargo, hay consideraciones especiales cuando un proveedor llama a la implementación wmi de un [**método IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) desde dentro de su propia implementación del mismo método. Estas consideraciones son importantes independientemente de si el proveedor llama a la versión sincrónica o asincrónica del método.

Cada [**método IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que un proveedor puede implementar tiene un parámetro *pCtx,* un puntero a una implementación de interfaz [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) Cuando WMI llama al proveedor, WMI pasa un puntero válido en este parámetro. Un proveedor siempre debe pasar este mismo puntero en las llamadas a WMI que realicen al atender las solicitudes. Si no se establece *pCtx correctamente,* WMI puede iniciar un bucle infinito.

En el ejemplo de código siguiente se muestra la manera correcta de llamar a la implementación wmi de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) desde una implementación [**de GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



El ejemplo de código de C++ de este tema requiere las siguientes referencias e \# instrucciones include para compilarse correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Los proveedores de instancias, clases y propiedades no deben emitir ninguna llamada a WMI que solicite la modificación de datos mientras se da servicio a una solicitud de lectura. Los únicos proveedores que son excepciones a esta regla son los proveedores de inserción. Un proveedor de inserción es un proveedor de clases que almacena datos en el repositorio WMI y se basa en WMI para controlar las solicitudes de los clientes. Al atender una solicitud de lectura, un proveedor de inserción puede actualizar el repositorio WMI, pero debe establecer el parámetro *lFlags* en **WBEM \_ FLAG OWNER \_ \_ UPDATE** en la llamada [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) adecuada.

Los proveedores de eventos no deben realizar ningún cambio de clase durante el mantenimiento de una llamada. Tampoco pueden emitir llamadas relacionadas con eventos, como modificar un filtro de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Establecer descriptores de seguridad namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 



